# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.0.1-rc.1] - 2025-09-13

### Fixed

#### DateTime Validation Bug Fix

- **Critical Fix**: Fixed DateTime validation issue in `setCreatedAt()` methods across multiple model classes
- **Problem**: The validation logic was incorrectly using `mb_strlen()` on DateTime objects, which expects string parameters, causing fatal errors when DateTime objects were passed to setter methods
- **Solution**: Enhanced validation to properly handle both DateTime objects and strings:
  - DateTime objects are converted to ISO 8601 format strings using `format('c')` before validation
  - String values are cast to string type before length validation
  - Maintains backward compatibility with existing string-based usage
  - Preserves all existing validation rules and error messages

#### Affected Files

- `lib/Model/SignatureRequest.php` - Fixed `setCreatedAt()` method (line 763)
- `lib/Model/SignatureRequestActivated.php` - Fixed `setCreatedAt()` method (line 709)  
- `lib/Model/SignatureRequestInList.php` - Fixed `setCreatedAt()` method (line 742)

#### Technical Details

**Before (Broken)**:
```php
if ((mb_strlen($created_at) < 1)) {
    throw new \InvalidArgumentException('invalid length for $created_at when calling SignatureRequest., must be bigger than or equal to 1.');
}
```

**After (Fixed)**:
```php
// Handle DateTime objects properly
if ($created_at instanceof \DateTime) {
    $created_at_string = $created_at->format('c'); // Convert to ISO 8601 string
} else {
    $created_at_string = (string) $created_at;
}

// Only validate string length if it's actually a string
if (is_string($created_at_string) && (mb_strlen($created_at_string) < 1)) {
    throw new \InvalidArgumentException('invalid length for $created_at when calling SignatureRequest., must be bigger than or equal to 1.');
}
```

#### Impact

- ✅ **Resolves Fatal Errors**: Eliminates `mb_strlen() expects parameter 1 to be string, object given` errors
- ✅ **Maintains Compatibility**: Existing code using string values continues to work unchanged
- ✅ **Enables DateTime Usage**: DateTime objects can now be properly passed to `setCreatedAt()` methods
- ✅ **Preserves Validation**: All existing validation rules and error messages remain intact
- ✅ **Standards Compliant**: DateTime objects are converted to ISO 8601 format for consistency

#### Testing

- Verified PHP syntax correctness for all modified files
- Confirmed no linting errors introduced
- All validation logic preserved and enhanced

---

**Note**: This is a release candidate. Please test thoroughly in your development environment before using in production.
