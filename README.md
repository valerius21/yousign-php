# OpenAPIClient-php

Build the best experience of digital signature through your own platform. Increase your conversion rates, leverage your data and reduce your costs with Yousign API.

For more information, please visit [https://yousign.com/contact](https://yousign.com/contact).

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure Bearer authorization: bearerAuth
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ApproverApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$signature_request_id = 'signature_request_id_example'; // string | Signature Request Id
$approver_id = 'approver_id_example'; // string | Approver Id

try {
    $apiInstance->deleteSignatureRequestsSignatureRequestIdApproversApproverId($signature_request_id, $approver_id);
} catch (Exception $e) {
    echo 'Exception when calling ApproverApi->deleteSignatureRequestsSignatureRequestIdApproversApproverId: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api-sandbox.yousign.app/v3*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ApproverApi* | [**deleteSignatureRequestsSignatureRequestIdApproversApproverId**](docs/Api/ApproverApi.md#deletesignaturerequestssignaturerequestidapproversapproverid) | **DELETE** /signature_requests/{signatureRequestId}/approvers/{approverId} | Delete an Approver
*ApproverApi* | [**getSignatureRequestsSignatureRequestIdApproversApproverId**](docs/Api/ApproverApi.md#getsignaturerequestssignaturerequestidapproversapproverid) | **GET** /signature_requests/{signatureRequestId}/approvers/{approverId} | Get an Approver
*ApproverApi* | [**patchSignatureRequestsSignatureRequestIdApproversApproverId**](docs/Api/ApproverApi.md#patchsignaturerequestssignaturerequestidapproversapproverid) | **PATCH** /signature_requests/{signatureRequestId}/approvers/{approverId} | Update an Approver
*ApproverApi* | [**postSignatureRequestsSignatureRequestIdApprovers**](docs/Api/ApproverApi.md#postsignaturerequestssignaturerequestidapprovers) | **POST** /signature_requests/{signatureRequestId}/approvers | Create a new Approver
*ApproverApi* | [**postSignatureRequestsSignatureRequestIdApproversApproverIdSendReminder**](docs/Api/ApproverApi.md#postsignaturerequestssignaturerequestidapproversapproveridsendreminder) | **POST** /signature_requests/{signatureRequestId}/approvers/{approverId}/send_reminder | Send manual reminder to an Approver
*ArchiveApi* | [**getArchivesArchivedFileIdDownload**](docs/Api/ArchiveApi.md#getarchivesarchivedfileiddownload) | **GET** /archives/{archivedFileId}/download | Download archived file
*ArchiveApi* | [**postArchives**](docs/Api/ArchiveApi.md#postarchives) | **POST** /archives | Direct upload an archived file
*AuditTrailApi* | [**getSignatureRequestsSignatureRequestIdAuditTrailsDownload**](docs/Api/AuditTrailApi.md#getsignaturerequestssignaturerequestidaudittrailsdownload) | **GET** /signature_requests/{signatureRequestId}/audit_trails/download | Download Signature Request Audit Trails
*AuditTrailApi* | [**getSignatureRequestsSignatureRequestIdSignersSignerIdAuditTrails**](docs/Api/AuditTrailApi.md#getsignaturerequestssignaturerequestidsignerssigneridaudittrails) | **GET** /signature_requests/{signatureRequestId}/signers/{signerId}/audit_trails | Get Signer Audit Trail
*AuditTrailApi* | [**getSignersSignerIdAuditTrailsDownload**](docs/Api/AuditTrailApi.md#getsignerssigneridaudittrailsdownload) | **GET** /signature_requests/{signatureRequestId}/signers/{signerId}/audit_trails/download | Download Audit Trail PDF
*BankAccountConnectionVerificationApi* | [**getVerificationsBankAccountConnections**](docs/Api/BankAccountConnectionVerificationApi.md#getverificationsbankaccountconnections) | **GET** /verifications/bank_account_connections | List Bank Account Connection Verifications
*BankAccountConnectionVerificationApi* | [**getVerificationsBankAccountConnectionsId**](docs/Api/BankAccountConnectionVerificationApi.md#getverificationsbankaccountconnectionsid) | **GET** /verifications/bank_account_connections/{verificationId} | Retrieve a Bank Account Connection Verification
*BankAccountConnectionVerificationApi* | [**postVerificationsBankAccountConnections**](docs/Api/BankAccountConnectionVerificationApi.md#postverificationsbankaccountconnections) | **POST** /verifications/bank_account_connections | Initiate a new Bank Account Connection
*BankAccountLookupVerificationApi* | [**getVerificationsBankAccountLookups**](docs/Api/BankAccountLookupVerificationApi.md#getverificationsbankaccountlookups) | **GET** /verifications/bank_account_lookups | List Bank Account Lookup Verifications
*BankAccountLookupVerificationApi* | [**getVerificationsBankAccountLookupsId**](docs/Api/BankAccountLookupVerificationApi.md#getverificationsbankaccountlookupsid) | **GET** /verifications/bank_account_lookups/{bankAccountLookupVerificationId} | Retrieve a Bank Account Lookup Verification
*BankAccountLookupVerificationApi* | [**postVerificationsBankAccountLookups**](docs/Api/BankAccountLookupVerificationApi.md#postverificationsbankaccountlookups) | **POST** /verifications/bank_account_lookups | Initiate a new Bank Account Lookup Verification
*BankAccountVerificationApi* | [**getVerificationsBankAccounts**](docs/Api/BankAccountVerificationApi.md#getverificationsbankaccounts) | **GET** /verifications/bank_accounts | List Bank Account Verifications
*BankAccountVerificationApi* | [**getVerificationsBankAccountsId**](docs/Api/BankAccountVerificationApi.md#getverificationsbankaccountsid) | **GET** /verifications/bank_accounts/{bankAccountVerificationId} | Retrieve a Bank Account Verification
*BankAccountVerificationApi* | [**postVerificationsBankAccounts**](docs/Api/BankAccountVerificationApi.md#postverificationsbankaccounts) | **POST** /verifications/bank_accounts | Initiate a new Bank Account Verification
*CompanyVerificationApi* | [**getVerificationsCompanies**](docs/Api/CompanyVerificationApi.md#getverificationscompanies) | **GET** /verifications/companies | List Company Verifications
*CompanyVerificationApi* | [**getVerificationsCompaniesId**](docs/Api/CompanyVerificationApi.md#getverificationscompaniesid) | **GET** /verifications/companies/{companyVerificationId} | Retrieve a Company Verification
*CompanyVerificationApi* | [**postVerificationsCompanies**](docs/Api/CompanyVerificationApi.md#postverificationscompanies) | **POST** /verifications/companies | Initiate a new Company Verification
*ConsumptionApi* | [**getConsumptionAddon**](docs/Api/ConsumptionApi.md#getconsumptionaddon) | **GET** /consumptions/addons | Get detailed addon consumption.
*ConsumptionApi* | [**getConsumptionDetail**](docs/Api/ConsumptionApi.md#getconsumptiondetail) | **GET** /consumptions/detail | Get detailed Consumption data
*ConsumptionApi* | [**getConsumptions**](docs/Api/ConsumptionApi.md#getconsumptions) | **GET** /consumptions | Get Consumptions
*ConsumptionApi* | [**getConsumptionsExport**](docs/Api/ConsumptionApi.md#getconsumptionsexport) | **GET** /consumptions/export | Export Consumption data
*ContactApi* | [**deleteContactsContactId**](docs/Api/ContactApi.md#deletecontactscontactid) | **DELETE** /contacts/{contactId} | Delete a Contact
*ContactApi* | [**getContacts**](docs/Api/ContactApi.md#getcontacts) | **GET** /contacts | List Contacts
*ContactApi* | [**getContactsContactId**](docs/Api/ContactApi.md#getcontactscontactid) | **GET** /contacts/{contactId} | Get a Contact
*ContactApi* | [**patchContactsContactId**](docs/Api/ContactApi.md#patchcontactscontactid) | **PATCH** /contacts/{contactId} | Update a Contact
*ContactApi* | [**postContact**](docs/Api/ContactApi.md#postcontact) | **POST** /contacts | Create a Contact
*CustomExperienceApi* | [**deleteCustomExperience**](docs/Api/CustomExperienceApi.md#deletecustomexperience) | **DELETE** /custom_experiences/{customExperienceId} | Delete a Custom Experience
*CustomExperienceApi* | [**deleteCustomExperienceLogo**](docs/Api/CustomExperienceApi.md#deletecustomexperiencelogo) | **DELETE** /custom_experiences/{customExperienceId}/logo | Delete a Custom Experience logo
*CustomExperienceApi* | [**getCustomExperiences**](docs/Api/CustomExperienceApi.md#getcustomexperiences) | **GET** /custom_experiences | List Custom Experiences
*CustomExperienceApi* | [**getCustomExperiencesCustomExperienceId**](docs/Api/CustomExperienceApi.md#getcustomexperiencescustomexperienceid) | **GET** /custom_experiences/{customExperienceId} | Get a Custom Experience
*CustomExperienceApi* | [**patchCustomExperienceLogo**](docs/Api/CustomExperienceApi.md#patchcustomexperiencelogo) | **POST** /custom_experiences/{customExperienceId}/logo | Update a Custom Experience logo
*CustomExperienceApi* | [**patchCustomExperiencesCustomExperienceId**](docs/Api/CustomExperienceApi.md#patchcustomexperiencescustomexperienceid) | **PATCH** /custom_experiences/{customExperienceId} | Update a Custom Experience
*CustomExperienceApi* | [**postCustomExperience**](docs/Api/CustomExperienceApi.md#postcustomexperience) | **POST** /custom_experiences | Create a Custom Experience
*DeprecatedApi* | [**createIdDocumentVerification**](docs/Api/DeprecatedApi.md#createiddocumentverification) | **POST** /id_document_verifications | [DEPRECATED] Initiate a new ID document verification
*DeprecatedApi* | [**getBankAccountVerifications**](docs/Api/DeprecatedApi.md#getbankaccountverifications) | **GET** /bank_account_verifications | [DEPRECATED] List Bank Account Verifications
*DeprecatedApi* | [**getBankAccountVerificationsBankAccountVerificationId**](docs/Api/DeprecatedApi.md#getbankaccountverificationsbankaccountverificationid) | **GET** /bank_account_verifications/{bankAccountVerificationId} | [DEPRECATED] Retrieve a bank account verification
*DeprecatedApi* | [**getIdDocumentVerification**](docs/Api/DeprecatedApi.md#getiddocumentverification) | **GET** /id_document_verifications/{idDocumentVerificationId} | [DEPRECATED] Retrieve an ID document verification
*DeprecatedApi* | [**getIdDocumentVerifications**](docs/Api/DeprecatedApi.md#getiddocumentverifications) | **GET** /id_document_verifications | [DEPRECATED] List ID Document Verifications
*DeprecatedApi* | [**postBankAccountVerifications**](docs/Api/DeprecatedApi.md#postbankaccountverifications) | **POST** /bank_account_verifications | [DEPRECATED] Initiate a new Bank Account Verification
*DeprecatedApi* | [**postDocuments**](docs/Api/DeprecatedApi.md#postdocuments) | **POST** /documents | [DEPRECATED] Upload a Document
*DocumentApi* | [**deleteSignatureRequestsSignatureRequestIdDocumentsDocumentId**](docs/Api/DocumentApi.md#deletesignaturerequestssignaturerequestiddocumentsdocumentid) | **DELETE** /signature_requests/{signatureRequestId}/documents/{documentId} | Delete a Document
*DocumentApi* | [**getSignatureRequestsSignatureRequestIdDocuments**](docs/Api/DocumentApi.md#getsignaturerequestssignaturerequestiddocuments) | **GET** /signature_requests/{signatureRequestId}/documents | List Signature Request&#39;s Documents
*DocumentApi* | [**getSignatureRequestsSignatureRequestIdDocumentsDocumentId**](docs/Api/DocumentApi.md#getsignaturerequestssignaturerequestiddocumentsdocumentid) | **GET** /signature_requests/{signatureRequestId}/documents/{documentId} | Get a Document
*DocumentApi* | [**getSignatureRequestsSignatureRequestIdDocumentsDocumentsIdDownload**](docs/Api/DocumentApi.md#getsignaturerequestssignaturerequestiddocumentsdocumentsiddownload) | **GET** /signature_requests/{signatureRequestId}/documents/{documentId}/download | Download a single Signature Request&#39;s Document
*DocumentApi* | [**getSignatureRequestsSignatureRequestIdDocumentsDownload**](docs/Api/DocumentApi.md#getsignaturerequestssignaturerequestiddocumentsdownload) | **GET** /signature_requests/{signatureRequestId}/documents/download | Download Signature Request&#39;s Documents
*DocumentApi* | [**patchSignatureRequestsSignatureRequestIdDocumentsDocumentId**](docs/Api/DocumentApi.md#patchsignaturerequestssignaturerequestiddocumentsdocumentid) | **PATCH** /signature_requests/{signatureRequestId}/documents/{documentId} | Update a Document
*DocumentApi* | [**postSignatureRequestsSignatureRequestIdDocuments**](docs/Api/DocumentApi.md#postsignaturerequestssignaturerequestiddocuments) | **POST** /signature_requests/{signatureRequestId}/documents | Add a sealed Document to a Signature Request
*DocumentApi* | [**postSignatureRequestsSignatureRequestIdDocumentsDocumentIdReplace**](docs/Api/DocumentApi.md#postsignaturerequestssignaturerequestiddocumentsdocumentidreplace) | **POST** /signature_requests/{signatureRequestId}/documents/{documentId}/replace | Replace a Document in a Signature Request
*ElectronicSealApi* | [**getElectronicSeal**](docs/Api/ElectronicSealApi.md#getelectronicseal) | **GET** /electronic_seals/{electronicSealId} | Get an Electronic Seal
*ElectronicSealApi* | [**listElectronicSealImages**](docs/Api/ElectronicSealApi.md#listelectronicsealimages) | **GET** /electronic_seal_images | List Electronic Seal Images
*ElectronicSealApi* | [**postElectronicSeals**](docs/Api/ElectronicSealApi.md#postelectronicseals) | **POST** /electronic_seals | Create an Electronic Seal
*ElectronicSealAuditTrailApi* | [**downloadElectronicSealAuditTrail**](docs/Api/ElectronicSealAuditTrailApi.md#downloadelectronicsealaudittrail) | **GET** /electronic_seals/{electronicSealId}/audit_trails/download | Download an Electronic Seal Audit Trail
*ElectronicSealAuditTrailApi* | [**getElectronicSealAuditTrail**](docs/Api/ElectronicSealAuditTrailApi.md#getelectronicsealaudittrail) | **GET** /electronic_seals/{electronicSealId}/audit_trails | Get an Electronic Seal Audit Trail
*ElectronicSealDocumentApi* | [**downloadElectronicSealDocument**](docs/Api/ElectronicSealDocumentApi.md#downloadelectronicsealdocument) | **GET** /electronic_seal_documents/{electronicSealDocumentId}/download | Download an Electronic Seal Document
*ElectronicSealDocumentApi* | [**uploadElectronicSealDocument**](docs/Api/ElectronicSealDocumentApi.md#uploadelectronicsealdocument) | **POST** /electronic_seal_documents | Create an Electronic Seal Document
*ElectronicSealImageApi* | [**deleteElectronicSealImage**](docs/Api/ElectronicSealImageApi.md#deleteelectronicsealimage) | **DELETE** /electronic_seal_images/{electronicSealImageId} | Delete an Electronic Seal Image
*ElectronicSealImageApi* | [**downloadElectronicSealImage**](docs/Api/ElectronicSealImageApi.md#downloadelectronicsealimage) | **GET** /electronic_seal_images/{electronicSealImageId}/download | Download an Electronic Seal Image
*ElectronicSealImageApi* | [**uploadElectronicSealImage**](docs/Api/ElectronicSealImageApi.md#uploadelectronicsealimage) | **POST** /electronic_seal_images | Upload an Electronic Seal Image
*FieldApi* | [**deleteSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId**](docs/Api/FieldApi.md#deletesignaturerequestssignaturerequestiddocumentsdocumentidfieldsfieldid) | **DELETE** /signature_requests/{signatureRequestId}/documents/{documentId}/fields/{fieldId} | Delete a Field
*FieldApi* | [**getSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields**](docs/Api/FieldApi.md#getsignaturerequestssignaturerequestiddocumentsdocumentidfields) | **GET** /signature_requests/{signatureRequestId}/documents/{documentId}/fields | Lists the Fields of a Signature Request Document.
*FieldApi* | [**postSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields**](docs/Api/FieldApi.md#postsignaturerequestssignaturerequestiddocumentsdocumentidfields) | **POST** /signature_requests/{signatureRequestId}/documents/{documentId}/fields | Create a new Field on a Document
*FieldApi* | [**signatureRequestsIdDocumentsIdFieldsIdAnswer**](docs/Api/FieldApi.md#signaturerequestsiddocumentsidfieldsidanswer) | **POST** /signature_requests/{signatureRequestId}/documents/{documentId}/fields/{fieldId}/answer | Answer a Field
*FieldApi* | [**updateSignatureRequestsSignatureRequestIdDocumentsDocumentIdFieldsFieldId**](docs/Api/FieldApi.md#updatesignaturerequestssignaturerequestiddocumentsdocumentidfieldsfieldid) | **PATCH** /signature_requests/{signatureRequestId}/documents/{documentId}/fields/{fieldId} | Update a Field
*FollowerApi* | [**getSignatureRequestsSignatureRequestIdFollowers**](docs/Api/FollowerApi.md#getsignaturerequestssignaturerequestidfollowers) | **GET** /signature_requests/{signatureRequestId}/followers | List the Signature Request&#39;s Followers
*FollowerApi* | [**postSignatureRequestsSignatureRequestIdFollowers**](docs/Api/FollowerApi.md#postsignaturerequestssignaturerequestidfollowers) | **POST** /signature_requests/{signatureRequestId}/followers | Create new Followers
*IdentityDocumentVerificationApi* | [**getVerificationsIdentityDocuments**](docs/Api/IdentityDocumentVerificationApi.md#getverificationsidentitydocuments) | **GET** /verifications/identity_documents | List Identity Document Verifications
*IdentityDocumentVerificationApi* | [**getVerificationsIdentityDocumentsId**](docs/Api/IdentityDocumentVerificationApi.md#getverificationsidentitydocumentsid) | **GET** /verifications/identity_documents/{identityDocumentVerificationId} | Retrieve an Identity Document Verification
*IdentityDocumentVerificationApi* | [**postVerificationsIdentityDocuments**](docs/Api/IdentityDocumentVerificationApi.md#postverificationsidentitydocuments) | **POST** /verifications/identity_documents | Initiate a new Identity Document Verification
*IdentityVideoVerificationApi* | [**getVerificationsIdentityVideos**](docs/Api/IdentityVideoVerificationApi.md#getverificationsidentityvideos) | **GET** /verifications/identity_videos | List Identity Videos
*IdentityVideoVerificationApi* | [**getVerificationsIdentityVideosId**](docs/Api/IdentityVideoVerificationApi.md#getverificationsidentityvideosid) | **GET** /verifications/identity_videos/{identityVideoVerificationId} | Retrieve an Identity Video
*IdentityVideoVerificationApi* | [**postVerificationsIdentityVideos**](docs/Api/IdentityVideoVerificationApi.md#postverificationsidentityvideos) | **POST** /verifications/identity_videos | Initiate a new Identity Video
*LabelApi* | [**deleteLabelsId**](docs/Api/LabelApi.md#deletelabelsid) | **DELETE** /labels/{labelId} | Delete a Label
*LabelApi* | [**deleteSignatureRequestsIdLabelsId**](docs/Api/LabelApi.md#deletesignaturerequestsidlabelsid) | **DELETE** /signature_requests/{signatureRequestId}/labels/{labelId} | Remove Label from a Signature Request
*LabelApi* | [**getLabels**](docs/Api/LabelApi.md#getlabels) | **GET** /labels | List Labels
*LabelApi* | [**getLabelsId**](docs/Api/LabelApi.md#getlabelsid) | **GET** /labels/{labelId} | Get a Label
*LabelApi* | [**getSignatureRequestsIdLabels**](docs/Api/LabelApi.md#getsignaturerequestsidlabels) | **GET** /signature_requests/{signatureRequestId}/labels | List Labels of a Signature Request
*LabelApi* | [**patchLabelId**](docs/Api/LabelApi.md#patchlabelid) | **PATCH** /labels/{labelId} | Update a Label
*LabelApi* | [**postLabels**](docs/Api/LabelApi.md#postlabels) | **POST** /labels | Create a new Label
*LabelApi* | [**putSignatureRequestsIdLabelsId**](docs/Api/LabelApi.md#putsignaturerequestsidlabelsid) | **PUT** /signature_requests/{signatureRequestId}/labels/{labelId} | Associate a Label with a Signature Request
*MetadataApi* | [**deleteSignatureRequestsSignatureRequestIdMetadata**](docs/Api/MetadataApi.md#deletesignaturerequestssignaturerequestidmetadata) | **DELETE** /signature_requests/{signatureRequestId}/metadata | Delete the Signature Request Metadata
*MetadataApi* | [**getSignatureRequestsSignatureRequestIdMetadata**](docs/Api/MetadataApi.md#getsignaturerequestssignaturerequestidmetadata) | **GET** /signature_requests/{signatureRequestId}/metadata | Get the Signature Request Metadata
*MetadataApi* | [**postSignatureRequestsSignatureRequestIdMetadata**](docs/Api/MetadataApi.md#postsignaturerequestssignaturerequestidmetadata) | **POST** /signature_requests/{signatureRequestId}/metadata | Attach Metadata to a Signature Request
*MetadataApi* | [**putSignatureRequestsSignatureRequestIdMetadata**](docs/Api/MetadataApi.md#putsignaturerequestssignaturerequestidmetadata) | **PUT** /signature_requests/{signatureRequestId}/metadata | Update Metadata of a Signature Request
*ProofOfAddressVerificationApi* | [**getVerificationsProofsOfAddress**](docs/Api/ProofOfAddressVerificationApi.md#getverificationsproofsofaddress) | **GET** /verifications/proofs_of_address | List Proof of Address Verifications
*ProofOfAddressVerificationApi* | [**getVerificationsProofsOfAddressId**](docs/Api/ProofOfAddressVerificationApi.md#getverificationsproofsofaddressid) | **GET** /verifications/proofs_of_address/{proofOfAddressVerificationId} | Retrieve a Proof of Address Verification
*ProofOfAddressVerificationApi* | [**postVerificationsProofsOfAddress**](docs/Api/ProofOfAddressVerificationApi.md#postverificationsproofsofaddress) | **POST** /verifications/proofs_of_address | Initiate a new Proof of Address Verification
*SignatureRequestApi* | [**deleteSignatureRequestsSignatureRequestId**](docs/Api/SignatureRequestApi.md#deletesignaturerequestssignaturerequestid) | **DELETE** /signature_requests/{signatureRequestId} | Delete a Signature Request
*SignatureRequestApi* | [**getSignatureRequests**](docs/Api/SignatureRequestApi.md#getsignaturerequests) | **GET** /signature_requests | List Signature Requests
*SignatureRequestApi* | [**getSignatureRequestsSignatureRequestId**](docs/Api/SignatureRequestApi.md#getsignaturerequestssignaturerequestid) | **GET** /signature_requests/{signatureRequestId} | Fetch a Signature Request
*SignatureRequestApi* | [**patchSignatureRequestsSignatureRequestId**](docs/Api/SignatureRequestApi.md#patchsignaturerequestssignaturerequestid) | **PATCH** /signature_requests/{signatureRequestId} | Update a Signature Request
*SignatureRequestApi* | [**postSignatureRequests**](docs/Api/SignatureRequestApi.md#postsignaturerequests) | **POST** /signature_requests | Initiate a new Signature Request
*SignatureRequestApi* | [**postSignatureRequestsSignatureRequestIdActivate**](docs/Api/SignatureRequestApi.md#postsignaturerequestssignaturerequestidactivate) | **POST** /signature_requests/{signatureRequestId}/activate | Activate a Signature Request
*SignatureRequestApi* | [**postSignatureRequestsSignatureRequestIdCancel**](docs/Api/SignatureRequestApi.md#postsignaturerequestssignaturerequestidcancel) | **POST** /signature_requests/{signatureRequestId}/cancel | Cancel a Signature Request
*SignatureRequestApi* | [**postSignatureRequestsSignatureRequestIdReactivate**](docs/Api/SignatureRequestApi.md#postsignaturerequestssignaturerequestidreactivate) | **POST** /signature_requests/{signatureRequestId}/reactivate | Reactivate an expired Signature Request
*SignerApi* | [**deleteSignatureRequestsSignatureRequestIdSignersSignerId**](docs/Api/SignerApi.md#deletesignaturerequestssignaturerequestidsignerssignerid) | **DELETE** /signature_requests/{signatureRequestId}/signers/{signerId} | Delete a Signer
*SignerApi* | [**getSignatureRequestsSignatureRequestIdSigners**](docs/Api/SignerApi.md#getsignaturerequestssignaturerequestidsigners) | **GET** /signature_requests/{signatureRequestId}/signers | List Signature Request&#39;s Signers
*SignerApi* | [**getSignersSignersId**](docs/Api/SignerApi.md#getsignerssignersid) | **GET** /signature_requests/{signatureRequestId}/signers/{signerId} | Get a Signer
*SignerApi* | [**patchSignatureRequestsSignatureRequestIdSignersSignerId**](docs/Api/SignerApi.md#patchsignaturerequestssignaturerequestidsignerssignerid) | **PATCH** /signature_requests/{signatureRequestId}/signers/{signerId} | Update a Signer
*SignerApi* | [**postSignatureRequestsIdSignersIdIdentityVerification**](docs/Api/SignerApi.md#postsignaturerequestsidsignersididentityverification) | **POST** /signature_requests/{signatureRequestId}/signers/{signerId}/identity_verification | Pre-verify an identity document
*SignerApi* | [**postSignatureRequestsIdSignersIdUnblockIdentification**](docs/Api/SignerApi.md#postsignaturerequestsidsignersidunblockidentification) | **POST** /signature_requests/{signatureRequestId}/signers/{signerId}/unblock_identification | Unblock Signer after an identity mismatch
*SignerApi* | [**postSignatureRequestsSignatureRequestIdSigners**](docs/Api/SignerApi.md#postsignaturerequestssignaturerequestidsigners) | **POST** /signature_requests/{signatureRequestId}/signers | Create a new Signer
*SignerApi* | [**postSignatureRequestsSignatureRequestIdSignersSignerIdSendOtp**](docs/Api/SignerApi.md#postsignaturerequestssignaturerequestidsignerssigneridsendotp) | **POST** /signature_requests/{signatureRequestId}/signers/{signerId}/send_otp | Send a One-Time Password (OTP) to a Signer
*SignerApi* | [**postSignatureRequestsSignatureRequestIdSignersSignerIdSendReminder**](docs/Api/SignerApi.md#postsignaturerequestssignaturerequestidsignerssigneridsendreminder) | **POST** /signature_requests/{signatureRequestId}/signers/{signerId}/send_reminder | Send manual reminder to a Signer
*SignerApi* | [**postSignatureRequestsSignatureRequestIdSignersSignerIdSign**](docs/Api/SignerApi.md#postsignaturerequestssignaturerequestidsignerssigneridsign) | **POST** /signature_requests/{signatureRequestId}/signers/{signerId}/sign | Sign a Signature Request
*SignerConsentRequestApi* | [**deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId**](docs/Api/SignerConsentRequestApi.md#deletesignaturerequestssignaturerequestidconsentrequestsconsentrequestid) | **DELETE** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId} | Delete a Signer Consent Request
*SignerConsentRequestApi* | [**deleteSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId**](docs/Api/SignerConsentRequestApi.md#deletesignaturerequestssignaturerequestidconsentrequestsconsentrequestidsignerssignerid) | **DELETE** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId}/signers/{signerId} | Remove a Signer from a given Signer Consent Request
*SignerConsentRequestApi* | [**getSignatureRequestsSignatureRequestIdSignerConsentRequests**](docs/Api/SignerConsentRequestApi.md#getsignaturerequestssignaturerequestidsignerconsentrequests) | **GET** /signature_requests/{signatureRequestId}/consent_requests | List Signer Consent Requests of the Signature Request
*SignerConsentRequestApi* | [**patchSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestId**](docs/Api/SignerConsentRequestApi.md#patchsignaturerequestssignaturerequestidconsentrequestsconsentrequestid) | **PATCH** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId} | Update a Signer Consent Request
*SignerConsentRequestApi* | [**postSignatureRequestsSignatureRequestIdConsentRequests**](docs/Api/SignerConsentRequestApi.md#postsignaturerequestssignaturerequestidconsentrequests) | **POST** /signature_requests/{signatureRequestId}/consent_requests | Add Signer Consent Request to a Signature Request
*SignerConsentRequestApi* | [**putSignatureRequestsSignatureRequestIdConsentRequestsConsentRequestIdSignersSignerId**](docs/Api/SignerConsentRequestApi.md#putsignaturerequestssignaturerequestidconsentrequestsconsentrequestidsignerssignerid) | **PUT** /signature_requests/{signatureRequestId}/consent_requests/{consentRequestId}/signers/{signerId} | Adds a Signer to a given Signer Consent Request
*SignerDocumentRequestApi* | [**deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestId**](docs/Api/SignerDocumentRequestApi.md#deletesignaturerequestssignaturerequestiddocumentrequestsdocumentrequestid) | **DELETE** /signature_requests/{signatureRequestId}/document_requests/{documentRequestId} | Delete a Signer Document Request
*SignerDocumentRequestApi* | [**deleteSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId**](docs/Api/SignerDocumentRequestApi.md#deletesignaturerequestssignaturerequestiddocumentrequestsdocumentrequestidsignerssignerid) | **DELETE** /signature_requests/{signatureRequestId}/document_requests/{documentRequestId}/signers/{signerId} | Remove a Signer to a given Signer Document Request
*SignerDocumentRequestApi* | [**deleteSignatureRequestsSignatureRequestIdSignersSignerIdDocuments**](docs/Api/SignerDocumentRequestApi.md#deletesignaturerequestssignaturerequestidsignerssigneriddocuments) | **DELETE** /signature_requests/{signatureRequestId}/signers/{signerId}/documents | Delete the Documents uploaded by a Signer
*SignerDocumentRequestApi* | [**getSignatureRequestsSignatureRequestIdSignerDocumentRequests**](docs/Api/SignerDocumentRequestApi.md#getsignaturerequestssignaturerequestidsignerdocumentrequests) | **GET** /signature_requests/{signatureRequestId}/document_requests | List Signer Document Requests of the Signature Request
*SignerDocumentRequestApi* | [**getSignatureRequestsSignatureRequestIdSignersSignerIdDocuments**](docs/Api/SignerDocumentRequestApi.md#getsignaturerequestssignaturerequestidsignerssigneriddocuments) | **GET** /signature_requests/{signatureRequestId}/signers/{signerId}/documents | List the Signer Documents of a Signer
*SignerDocumentRequestApi* | [**getSignatureRequestsSignatureRequestIdSignersSignerIdDocumentsSignerDocumentId**](docs/Api/SignerDocumentRequestApi.md#getsignaturerequestssignaturerequestidsignerssigneriddocumentssignerdocumentid) | **GET** /signature_requests/{signatureRequestId}/signers/{signerId}/documents/{signerDocumentId}/download | Download a Signer Document
*SignerDocumentRequestApi* | [**postSignatureRequestsSignatureRequestIdDocumentRequests**](docs/Api/SignerDocumentRequestApi.md#postsignaturerequestssignaturerequestiddocumentrequests) | **POST** /signature_requests/{signatureRequestId}/document_requests | Add Signer Document Request to a Signature Request
*SignerDocumentRequestApi* | [**putSignatureRequestsSignatureRequestIdDocumentRequestsDocumentRequestIdSignersSignerId**](docs/Api/SignerDocumentRequestApi.md#putsignaturerequestssignaturerequestiddocumentrequestsdocumentrequestidsignerssignerid) | **PUT** /signature_requests/{signatureRequestId}/document_requests/{documentRequestId}/signers/{signerId} | Adds a Signer to a given Signer Document Request
*TemplateApi* | [**getTemplates**](docs/Api/TemplateApi.md#gettemplates) | **GET** /templates | List Templates
*UserApi* | [**deleteUsersUserId**](docs/Api/UserApi.md#deleteusersuserid) | **DELETE** /users/{userId} | Delete a User
*UserApi* | [**deleteWorkspaceWorkspaceIdUsersUserId**](docs/Api/UserApi.md#deleteworkspaceworkspaceidusersuserid) | **DELETE** /workspaces/{workspaceId}/users/{userId} | Remove a user from a workspace
*UserApi* | [**getUsers**](docs/Api/UserApi.md#getusers) | **GET** /users | List Users
*UserApi* | [**getUsersUserId**](docs/Api/UserApi.md#getusersuserid) | **GET** /users/{userId} | Get a User
*UserApi* | [**patchUsersUserId**](docs/Api/UserApi.md#patchusersuserid) | **PATCH** /users/{userId} | Update a User
*UserApi* | [**postUsers**](docs/Api/UserApi.md#postusers) | **POST** /users | Create a new User
*UserApi* | [**putWorkspacesWorkspaceIdUsers**](docs/Api/UserApi.md#putworkspacesworkspaceidusers) | **PUT** /workspaces/{workspaceId}/users/{userId} | Associate a user to a workspace
*UserInvitationApi* | [**getInvitations**](docs/Api/UserInvitationApi.md#getinvitations) | **GET** /users/invitations | List User Invitations
*UserInvitationApi* | [**getUsersInvitationInvitationId**](docs/Api/UserInvitationApi.md#getusersinvitationinvitationid) | **GET** /users/invitations/{invitationId} | Get an Invitation
*UserInvitationApi* | [**getUsersUserIdInvitation**](docs/Api/UserInvitationApi.md#getusersuseridinvitation) | **GET** /users/{userId}/invitation | Get a User Invitation via the User
*WatchlistVerificationApi* | [**getVerificationsWatchlists**](docs/Api/WatchlistVerificationApi.md#getverificationswatchlists) | **GET** /verifications/watchlists | List Watchlist Verifications
*WatchlistVerificationApi* | [**getVerificationsWatchlistsId**](docs/Api/WatchlistVerificationApi.md#getverificationswatchlistsid) | **GET** /verifications/watchlists/{watchlistVerificationId} | Retrieve a Watchlist Verification
*WatchlistVerificationApi* | [**postVerificationsWatchlists**](docs/Api/WatchlistVerificationApi.md#postverificationswatchlists) | **POST** /verifications/watchlists | Initiate a Watchlist Verification
*WebhookApi* | [**deleteWebhooksWebhookId**](docs/Api/WebhookApi.md#deletewebhookswebhookid) | **DELETE** /webhooks/{webhookId} | Delete a Webhook subscription
*WebhookApi* | [**getWebhooks**](docs/Api/WebhookApi.md#getwebhooks) | **GET** /webhooks | List Webhook subscriptions
*WebhookApi* | [**getWebhooksWebhookId**](docs/Api/WebhookApi.md#getwebhookswebhookid) | **GET** /webhooks/{webhookId} | Get a Webhook subscription
*WebhookApi* | [**patchWebhooksWebhookId**](docs/Api/WebhookApi.md#patchwebhookswebhookid) | **PATCH** /webhooks/{webhookId} | Update a Webhook subscription
*WebhookApi* | [**postWebhooksSubscriptions**](docs/Api/WebhookApi.md#postwebhookssubscriptions) | **POST** /webhooks | Create a Webhook subscription
*WorkspaceApi* | [**deleteWorkspace**](docs/Api/WorkspaceApi.md#deleteworkspace) | **DELETE** /workspaces/{workspaceId} | Delete a Workspace
*WorkspaceApi* | [**getWorkspaces**](docs/Api/WorkspaceApi.md#getworkspaces) | **GET** /workspaces | List Workspaces
*WorkspaceApi* | [**getWorkspacesDefault**](docs/Api/WorkspaceApi.md#getworkspacesdefault) | **GET** /workspaces/default | Get the default Workspace
*WorkspaceApi* | [**getWorkspacesWorkspaceId**](docs/Api/WorkspaceApi.md#getworkspacesworkspaceid) | **GET** /workspaces/{workspaceId} | Get a Workspace
*WorkspaceApi* | [**markWorkspaceAsDefault**](docs/Api/WorkspaceApi.md#markworkspaceasdefault) | **POST** /workspaces/default | Mark the given Workspace as default
*WorkspaceApi* | [**patchWorkspacesWorkspaceId**](docs/Api/WorkspaceApi.md#patchworkspacesworkspaceid) | **PATCH** /workspaces/{workspaceId} | Update a Workspace
*WorkspaceApi* | [**postWorkspace**](docs/Api/WorkspaceApi.md#postworkspace) | **POST** /workspaces | Create a Workspace

## Models

- [ActivateSignatureRequest](docs/Model/ActivateSignatureRequest.md)
- [AddonConsumption](docs/Model/AddonConsumption.md)
- [Approver](docs/Model/Approver.md)
- [ApproverInfo](docs/Model/ApproverInfo.md)
- [ApproverToNotify](docs/Model/ApproverToNotify.md)
- [ArchivedFile](docs/Model/ArchivedFile.md)
- [Archiving](docs/Model/Archiving.md)
- [AuditTrailLocale](docs/Model/AuditTrailLocale.md)
- [BadRequestResponse](docs/Model/BadRequestResponse.md)
- [BankAccountConnectionFull](docs/Model/BankAccountConnectionFull.md)
- [BankAccountConnectionFullAllOfData](docs/Model/BankAccountConnectionFullAllOfData.md)
- [BankAccountConnectionFullAllOfDataParties](docs/Model/BankAccountConnectionFullAllOfDataParties.md)
- [BankAccountConnectionMeta](docs/Model/BankAccountConnectionMeta.md)
- [BankAccountConnectionStatus](docs/Model/BankAccountConnectionStatus.md)
- [BankAccountFull](docs/Model/BankAccountFull.md)
- [BankAccountFullAllOfData](docs/Model/BankAccountFullAllOfData.md)
- [BankAccountFullAllOfDataExtractedFromDocument](docs/Model/BankAccountFullAllOfDataExtractedFromDocument.md)
- [BankAccountLookupMeta](docs/Model/BankAccountLookupMeta.md)
- [BankAccountMeta](docs/Model/BankAccountMeta.md)
- [BankAccountStatus](docs/Model/BankAccountStatus.md)
- [Checkbox](docs/Model/Checkbox.md)
- [Checkbox1](docs/Model/Checkbox1.md)
- [Checkbox2](docs/Model/Checkbox2.md)
- [CompanyFull](docs/Model/CompanyFull.md)
- [CompanyFullAllOfData](docs/Model/CompanyFullAllOfData.md)
- [CompanyFullAllOfDataCompanyInformation](docs/Model/CompanyFullAllOfDataCompanyInformation.md)
- [CompanyFullAllOfDataCompanyInformationActivities](docs/Model/CompanyFullAllOfDataCompanyInformationActivities.md)
- [CompanyFullAllOfDataCompanyInformationCommercialRegistration](docs/Model/CompanyFullAllOfDataCompanyInformationCommercialRegistration.md)
- [CompanyFullAllOfDataCompanyInformationLegalForm](docs/Model/CompanyFullAllOfDataCompanyInformationLegalForm.md)
- [CompanyFullAllOfDataExtractedFromDocument](docs/Model/CompanyFullAllOfDataExtractedFromDocument.md)
- [CompanyFullAllOfDataHeadquarter](docs/Model/CompanyFullAllOfDataHeadquarter.md)
- [CompanyFullAllOfDataLegalRepresentatives](docs/Model/CompanyFullAllOfDataLegalRepresentatives.md)
- [CompanyMeta](docs/Model/CompanyMeta.md)
- [Consumption](docs/Model/Consumption.md)
- [ConsumptionApi](docs/Model/ConsumptionApi.md)
- [ConsumptionApp](docs/Model/ConsumptionApp.md)
- [ConsumptionAppQualifiedElectronicSignatureIdentificationMode](docs/Model/ConsumptionAppQualifiedElectronicSignatureIdentificationMode.md)
- [ConsumptionAppQualifiedElectronicSignatureIdentificationModeIdentityVerification](docs/Model/ConsumptionAppQualifiedElectronicSignatureIdentificationModeIdentityVerification.md)
- [Contact](docs/Model/Contact.md)
- [CreateApprover](docs/Model/CreateApprover.md)
- [CreateContact](docs/Model/CreateContact.md)
- [CreateCustomExperience](docs/Model/CreateCustomExperience.md)
- [CreateCustomExperienceRedirectUrls](docs/Model/CreateCustomExperienceRedirectUrls.md)
- [CreateDocumentFromJson](docs/Model/CreateDocumentFromJson.md)
- [CreateElectronicSealDocumentFromJson](docs/Model/CreateElectronicSealDocumentFromJson.md)
- [CreateElectronicSealFieldReadOnlyTextPayload](docs/Model/CreateElectronicSealFieldReadOnlyTextPayload.md)
- [CreateElectronicSealFieldSealPayload](docs/Model/CreateElectronicSealFieldSealPayload.md)
- [CreateElectronicSealPayload](docs/Model/CreateElectronicSealPayload.md)
- [CreateElectronicSealPayloadFieldsInner](docs/Model/CreateElectronicSealPayloadFieldsInner.md)
- [CreateField](docs/Model/CreateField.md)
- [CreateFieldFont](docs/Model/CreateFieldFont.md)
- [CreateFollowersInner](docs/Model/CreateFollowersInner.md)
- [CreateLabel](docs/Model/CreateLabel.md)
- [CreateSignatureRequest](docs/Model/CreateSignatureRequest.md)
- [CreateSignatureRequestReminderSettings](docs/Model/CreateSignatureRequestReminderSettings.md)
- [CreateSignatureRequestSignersInner](docs/Model/CreateSignatureRequestSignersInner.md)
- [CreateSignatureRequestTemplatePlaceholders](docs/Model/CreateSignatureRequestTemplatePlaceholders.md)
- [CreateSignatureRequestTemplatePlaceholdersSignersInner](docs/Model/CreateSignatureRequestTemplatePlaceholdersSignersInner.md)
- [CreateSigner](docs/Model/CreateSigner.md)
- [CreateSignerConsentRequest](docs/Model/CreateSignerConsentRequest.md)
- [CreateSignerConsentRequestSettings](docs/Model/CreateSignerConsentRequestSettings.md)
- [CreateSignerDocumentRequest](docs/Model/CreateSignerDocumentRequest.md)
- [CreateUser](docs/Model/CreateUser.md)
- [CreateWebhookSubscription](docs/Model/CreateWebhookSubscription.md)
- [CreateWebhookSubscriptionScopes](docs/Model/CreateWebhookSubscriptionScopes.md)
- [CreateWebhookSubscriptionSubscribedEvents](docs/Model/CreateWebhookSubscriptionSubscribedEvents.md)
- [CreateWebhookSubscriptionWorkspaces](docs/Model/CreateWebhookSubscriptionWorkspaces.md)
- [CreateWorkspace](docs/Model/CreateWorkspace.md)
- [CustomExperience](docs/Model/CustomExperience.md)
- [CustomExperienceDisabledNotificationsType](docs/Model/CustomExperienceDisabledNotificationsType.md)
- [CustomExperienceRedirectUrls](docs/Model/CustomExperienceRedirectUrls.md)
- [CustomExperienceSource](docs/Model/CustomExperienceSource.md)
- [CustomText](docs/Model/CustomText.md)
- [DeleteWorkspace](docs/Model/DeleteWorkspace.md)
- [DetailedConsumption](docs/Model/DetailedConsumption.md)
- [Document](docs/Model/Document.md)
- [DocumentInitials](docs/Model/DocumentInitials.md)
- [DocumentInitialsPerPageInner](docs/Model/DocumentInitialsPerPageInner.md)
- [ElectronicSeal](docs/Model/ElectronicSeal.md)
- [ElectronicSealAuditTrail](docs/Model/ElectronicSealAuditTrail.md)
- [ElectronicSealDocument](docs/Model/ElectronicSealDocument.md)
- [ElectronicSealImage](docs/Model/ElectronicSealImage.md)
- [EmailNotification](docs/Model/EmailNotification.md)
- [EmailNotification1](docs/Model/EmailNotification1.md)
- [EmbeddedSignerWithSignatureLink](docs/Model/EmbeddedSignerWithSignatureLink.md)
- [FieldAnswer](docs/Model/FieldAnswer.md)
- [FieldAnswerValue](docs/Model/FieldAnswerValue.md)
- [FieldCheckbox](docs/Model/FieldCheckbox.md)
- [FieldMention](docs/Model/FieldMention.md)
- [FieldRadioButtonGroup](docs/Model/FieldRadioButtonGroup.md)
- [FieldRadioButtonGroupRadiosInner](docs/Model/FieldRadioButtonGroupRadiosInner.md)
- [FieldReadOnlyText](docs/Model/FieldReadOnlyText.md)
- [FieldSignature](docs/Model/FieldSignature.md)
- [FieldText](docs/Model/FieldText.md)
- [FieldsInput](docs/Model/FieldsInput.md)
- [Follower](docs/Model/Follower.md)
- [Font](docs/Model/Font.md)
- [FontFamily](docs/Model/FontFamily.md)
- [FontVariants](docs/Model/FontVariants.md)
- [ForbiddenResponse](docs/Model/ForbiddenResponse.md)
- [FromElectronicSealDocument](docs/Model/FromElectronicSealDocument.md)
- [FromSignatureRequestDocument](docs/Model/FromSignatureRequestDocument.md)
- [GetBankAccountVerifications200Response](docs/Model/GetBankAccountVerifications200Response.md)
- [GetBankAccountVerifications200ResponseDataInner](docs/Model/GetBankAccountVerifications200ResponseDataInner.md)
- [GetBankAccountVerificationsBankAccountVerificationId200Response](docs/Model/GetBankAccountVerificationsBankAccountVerificationId200Response.md)
- [GetBankAccountVerificationsBankAccountVerificationId200ResponseAllOfExtractedFromDocument](docs/Model/GetBankAccountVerificationsBankAccountVerificationId200ResponseAllOfExtractedFromDocument.md)
- [GetConsumptionAddon200Response](docs/Model/GetConsumptionAddon200Response.md)
- [GetConsumptionDetail200Response](docs/Model/GetConsumptionDetail200Response.md)
- [GetContacts200Response](docs/Model/GetContacts200Response.md)
- [GetCustomExperiences200Response](docs/Model/GetCustomExperiences200Response.md)
- [GetIdDocumentVerification200Response](docs/Model/GetIdDocumentVerification200Response.md)
- [GetIdDocumentVerification200ResponseAllOfExtractedFromDocument](docs/Model/GetIdDocumentVerification200ResponseAllOfExtractedFromDocument.md)
- [GetIdDocumentVerification200ResponseAllOfExtractedFromDocumentMrz](docs/Model/GetIdDocumentVerification200ResponseAllOfExtractedFromDocumentMrz.md)
- [GetIdDocumentVerifications200Response](docs/Model/GetIdDocumentVerifications200Response.md)
- [GetIdDocumentVerifications200ResponseDataInner](docs/Model/GetIdDocumentVerifications200ResponseDataInner.md)
- [GetInvitations200Response](docs/Model/GetInvitations200Response.md)
- [GetLabels200Response](docs/Model/GetLabels200Response.md)
- [GetSignatureRequests200Response](docs/Model/GetSignatureRequests200Response.md)
- [GetSignatureRequestsIdLabels200Response](docs/Model/GetSignatureRequestsIdLabels200Response.md)
- [GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200Response](docs/Model/GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200Response.md)
- [GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner](docs/Model/GetSignatureRequestsSignatureRequestIdDocumentsDocumentIdFields200ResponseDataInner.md)
- [GetSignatureRequestsSignatureRequestIdFollowers200Response](docs/Model/GetSignatureRequestsSignatureRequestIdFollowers200Response.md)
- [GetSignatureRequestsSignatureRequestIdSignerConsentRequests200Response](docs/Model/GetSignatureRequestsSignatureRequestIdSignerConsentRequests200Response.md)
- [GetSignatureRequestsSignatureRequestIdSignerDocumentRequests200Response](docs/Model/GetSignatureRequestsSignatureRequestIdSignerDocumentRequests200Response.md)
- [GetSignatureRequestsSignatureRequestIdSignersSignerIdDocuments200Response](docs/Model/GetSignatureRequestsSignatureRequestIdSignersSignerIdDocuments200Response.md)
- [GetTemplates200Response](docs/Model/GetTemplates200Response.md)
- [GetUsers200Response](docs/Model/GetUsers200Response.md)
- [GetVerificationsBankAccountConnections200Response](docs/Model/GetVerificationsBankAccountConnections200Response.md)
- [GetVerificationsBankAccountLookups200Response](docs/Model/GetVerificationsBankAccountLookups200Response.md)
- [GetVerificationsBankAccounts200Response](docs/Model/GetVerificationsBankAccounts200Response.md)
- [GetVerificationsCompanies200Response](docs/Model/GetVerificationsCompanies200Response.md)
- [GetVerificationsIdentityDocuments200Response](docs/Model/GetVerificationsIdentityDocuments200Response.md)
- [GetVerificationsIdentityVideos200Response](docs/Model/GetVerificationsIdentityVideos200Response.md)
- [GetVerificationsProofsOfAddress200Response](docs/Model/GetVerificationsProofsOfAddress200Response.md)
- [GetVerificationsWatchlists200Response](docs/Model/GetVerificationsWatchlists200Response.md)
- [GetWorkspaces200Response](docs/Model/GetWorkspaces200Response.md)
- [IdentityDocumentFull](docs/Model/IdentityDocumentFull.md)
- [IdentityDocumentFullAllOfData](docs/Model/IdentityDocumentFullAllOfData.md)
- [IdentityDocumentFullAllOfDataExtractedFromDocument](docs/Model/IdentityDocumentFullAllOfDataExtractedFromDocument.md)
- [IdentityDocumentMeta](docs/Model/IdentityDocumentMeta.md)
- [IdentityDocumentStatus](docs/Model/IdentityDocumentStatus.md)
- [IdentityVideoDocument](docs/Model/IdentityVideoDocument.md)
- [IdentityVideoFull](docs/Model/IdentityVideoFull.md)
- [IdentityVideoFullAllOfData](docs/Model/IdentityVideoFullAllOfData.md)
- [IdentityVideoFullAllOfDataEvidence](docs/Model/IdentityVideoFullAllOfDataEvidence.md)
- [IdentityVideoMeta](docs/Model/IdentityVideoMeta.md)
- [IdentityVideoStatus](docs/Model/IdentityVideoStatus.md)
- [InitialsArea](docs/Model/InitialsArea.md)
- [InitiateBankAccountConnection](docs/Model/InitiateBankAccountConnection.md)
- [InitiateBankAccountConnectionWithLegalPerson](docs/Model/InitiateBankAccountConnectionWithLegalPerson.md)
- [InitiateBankAccountLookupWithLegalPerson](docs/Model/InitiateBankAccountLookupWithLegalPerson.md)
- [InitiateBankAccountLookupWithLegalPersonLegalPerson](docs/Model/InitiateBankAccountLookupWithLegalPersonLegalPerson.md)
- [InitiateBankAccountLookupWithNaturalPerson](docs/Model/InitiateBankAccountLookupWithNaturalPerson.md)
- [InitiateBankAccountLookupWithNaturalPersonNaturalPerson](docs/Model/InitiateBankAccountLookupWithNaturalPersonNaturalPerson.md)
- [InitiateBankAccountWithLegalPersonLegalPerson](docs/Model/InitiateBankAccountWithLegalPersonLegalPerson.md)
- [InitiateBankAccountWithNaturalPersonNaturalPerson](docs/Model/InitiateBankAccountWithNaturalPersonNaturalPerson.md)
- [InitiateCompanyFromJson](docs/Model/InitiateCompanyFromJson.md)
- [InitiateIdentityVideo](docs/Model/InitiateIdentityVideo.md)
- [InitiateProofOfAddressNaturalPerson](docs/Model/InitiateProofOfAddressNaturalPerson.md)
- [InitiateProofOfAddressNaturalPersonAddress](docs/Model/InitiateProofOfAddressNaturalPersonAddress.md)
- [InitiateWatchlist](docs/Model/InitiateWatchlist.md)
- [InitiateWatchlistNaturalPerson](docs/Model/InitiateWatchlistNaturalPerson.md)
- [InternalServerError](docs/Model/InternalServerError.md)
- [Label](docs/Model/Label.md)
- [LegacyBankAccountVerification](docs/Model/LegacyBankAccountVerification.md)
- [LegacyBankAccountVerificationCreated](docs/Model/LegacyBankAccountVerificationCreated.md)
- [LegacyBankAccountVerificationStatus](docs/Model/LegacyBankAccountVerificationStatus.md)
- [LegacyIdDocumentVerification](docs/Model/LegacyIdDocumentVerification.md)
- [LegacyIdDocumentVerificationCreated](docs/Model/LegacyIdDocumentVerificationCreated.md)
- [LegacyIdDocumentVerificationStatus](docs/Model/LegacyIdDocumentVerificationStatus.md)
- [ListElectronicSealImages200Response](docs/Model/ListElectronicSealImages200Response.md)
- [Locale](docs/Model/Locale.md)
- [LogoLayout](docs/Model/LogoLayout.md)
- [ManageableRole](docs/Model/ManageableRole.md)
- [MarkWorkspaceAsDefault](docs/Model/MarkWorkspaceAsDefault.md)
- [Mention](docs/Model/Mention.md)
- [Mention1](docs/Model/Mention1.md)
- [Mention2](docs/Model/Mention2.md)
- [Metadata](docs/Model/Metadata.md)
- [MetadataDataValue](docs/Model/MetadataDataValue.md)
- [MethodNotAllowed](docs/Model/MethodNotAllowed.md)
- [NewApproverFromExistingContact](docs/Model/NewApproverFromExistingContact.md)
- [NewApproverFromExistingSigner](docs/Model/NewApproverFromExistingSigner.md)
- [NewApproverFromExistingUser](docs/Model/NewApproverFromExistingUser.md)
- [NewApproverFromScratch](docs/Model/NewApproverFromScratch.md)
- [NewApproverFromScratchInfo](docs/Model/NewApproverFromScratchInfo.md)
- [NewSignerFromExistingContact](docs/Model/NewSignerFromExistingContact.md)
- [NewSignerFromExistingUser](docs/Model/NewSignerFromExistingUser.md)
- [NewSignerFromScratch](docs/Model/NewSignerFromScratch.md)
- [NewSignerFromScratchCustomText](docs/Model/NewSignerFromScratchCustomText.md)
- [NewSignerFromScratchInfo](docs/Model/NewSignerFromScratchInfo.md)
- [NewSignerFromScratchRedirectUrls](docs/Model/NewSignerFromScratchRedirectUrls.md)
- [NotFoundResponse](docs/Model/NotFoundResponse.md)
- [OTPMessage](docs/Model/OTPMessage.md)
- [OtpMessage](docs/Model/OtpMessage.md)
- [Pagination](docs/Model/Pagination.md)
- [PaginationWithUpdatedAt](docs/Model/PaginationWithUpdatedAt.md)
- [PostSignatureRequestsSignatureRequestIdCancelRequest](docs/Model/PostSignatureRequestsSignatureRequestIdCancelRequest.md)
- [PostSignatureRequestsSignatureRequestIdReactivateRequest](docs/Model/PostSignatureRequestsSignatureRequestIdReactivateRequest.md)
- [PostVerificationsBankAccountConnectionsRequest](docs/Model/PostVerificationsBankAccountConnectionsRequest.md)
- [PostVerificationsBankAccountLookupsRequest](docs/Model/PostVerificationsBankAccountLookupsRequest.md)
- [ProofOfAddressFull](docs/Model/ProofOfAddressFull.md)
- [ProofOfAddressFullAllOfData](docs/Model/ProofOfAddressFullAllOfData.md)
- [ProofOfAddressFullAllOfDataExtractedFromDocument](docs/Model/ProofOfAddressFullAllOfDataExtractedFromDocument.md)
- [ProofOfAddressFullAllOfDataExtractedFromDocument2dDoc](docs/Model/ProofOfAddressFullAllOfDataExtractedFromDocument2dDoc.md)
- [ProofOfAddressFullAllOfDataExtractedFromDocument2dDocAddress](docs/Model/ProofOfAddressFullAllOfDataExtractedFromDocument2dDocAddress.md)
- [ProofOfAddressMeta](docs/Model/ProofOfAddressMeta.md)
- [RadioGroup](docs/Model/RadioGroup.md)
- [RadioGroup1](docs/Model/RadioGroup1.md)
- [RadioGroup1RadiosInner](docs/Model/RadioGroup1RadiosInner.md)
- [RadioGroup2](docs/Model/RadioGroup2.md)
- [RadioGroup2RadiosInner](docs/Model/RadioGroup2RadiosInner.md)
- [RadioGroupRadiosInner](docs/Model/RadioGroupRadiosInner.md)
- [ReadOnlyText](docs/Model/ReadOnlyText.md)
- [ReadOnlyText1](docs/Model/ReadOnlyText1.md)
- [Signature](docs/Model/Signature.md)
- [Signature1](docs/Model/Signature1.md)
- [Signature2](docs/Model/Signature2.md)
- [SignatureRequest](docs/Model/SignatureRequest.md)
- [SignatureRequestActivated](docs/Model/SignatureRequestActivated.md)
- [SignatureRequestActivatedDocumentsInner](docs/Model/SignatureRequestActivatedDocumentsInner.md)
- [SignatureRequestDeclineInformation](docs/Model/SignatureRequestDeclineInformation.md)
- [SignatureRequestEmailNotification](docs/Model/SignatureRequestEmailNotification.md)
- [SignatureRequestEmailNotificationCustomText](docs/Model/SignatureRequestEmailNotificationCustomText.md)
- [SignatureRequestEmailNotificationSender](docs/Model/SignatureRequestEmailNotificationSender.md)
- [SignatureRequestInList](docs/Model/SignatureRequestInList.md)
- [SignatureRequestInListApproversInner](docs/Model/SignatureRequestInListApproversInner.md)
- [SignatureRequestInListDocumentsInner](docs/Model/SignatureRequestInListDocumentsInner.md)
- [SignatureRequestInListReminderSettings](docs/Model/SignatureRequestInListReminderSettings.md)
- [SignatureRequestInListSender](docs/Model/SignatureRequestInListSender.md)
- [SignatureRequestInListSignersInner](docs/Model/SignatureRequestInListSignersInner.md)
- [SignatureRequestLabel](docs/Model/SignatureRequestLabel.md)
- [SignatureRequestPlaceholderReadOnlyTextFieldSubstituteInput](docs/Model/SignatureRequestPlaceholderReadOnlyTextFieldSubstituteInput.md)
- [SignatureRequestPlaceholderSignerSubstituteFromContactIdInput](docs/Model/SignatureRequestPlaceholderSignerSubstituteFromContactIdInput.md)
- [SignatureRequestPlaceholderSignerSubstituteFromInfoInput](docs/Model/SignatureRequestPlaceholderSignerSubstituteFromInfoInput.md)
- [SignatureRequestPlaceholderSignerSubstituteFromInfoInputInfo](docs/Model/SignatureRequestPlaceholderSignerSubstituteFromInfoInputInfo.md)
- [SignatureRequestPlaceholderSignerSubstituteFromUserIdInput](docs/Model/SignatureRequestPlaceholderSignerSubstituteFromUserIdInput.md)
- [SignatureRequestSignerFromContactIdInput](docs/Model/SignatureRequestSignerFromContactIdInput.md)
- [SignatureRequestSignerFromInfoInput](docs/Model/SignatureRequestSignerFromInfoInput.md)
- [SignatureRequestSignerFromInfoInputCustomText](docs/Model/SignatureRequestSignerFromInfoInputCustomText.md)
- [SignatureRequestSignerFromInfoInputInfo](docs/Model/SignatureRequestSignerFromInfoInputInfo.md)
- [SignatureRequestSignerFromInfoInputRedirectUrls](docs/Model/SignatureRequestSignerFromInfoInputRedirectUrls.md)
- [SignatureRequestSignerFromUserIdInput](docs/Model/SignatureRequestSignerFromUserIdInput.md)
- [SignatureRequestStatus](docs/Model/SignatureRequestStatus.md)
- [Signer](docs/Model/Signer.md)
- [SignerAuditTrail](docs/Model/SignerAuditTrail.md)
- [SignerConsentRequest](docs/Model/SignerConsentRequest.md)
- [SignerConsentRequestSettings](docs/Model/SignerConsentRequestSettings.md)
- [SignerDeliveryMode](docs/Model/SignerDeliveryMode.md)
- [SignerDocument](docs/Model/SignerDocument.md)
- [SignerDocumentRequest](docs/Model/SignerDocumentRequest.md)
- [SignerFieldsInner](docs/Model/SignerFieldsInner.md)
- [SignerInfo](docs/Model/SignerInfo.md)
- [SignerRedirectUrls](docs/Model/SignerRedirectUrls.md)
- [SignerSIPAddress](docs/Model/SignerSIPAddress.md)
- [SignerSign](docs/Model/SignerSign.md)
- [SmsNotification](docs/Model/SmsNotification.md)
- [SmsNotification1](docs/Model/SmsNotification1.md)
- [Template](docs/Model/Template.md)
- [Text](docs/Model/Text.md)
- [Text1](docs/Model/Text1.md)
- [Text2](docs/Model/Text2.md)
- [TooManyRequestsResponse](docs/Model/TooManyRequestsResponse.md)
- [UnauthorizedResponse](docs/Model/UnauthorizedResponse.md)
- [UnsupportedMediaTypeResponse](docs/Model/UnsupportedMediaTypeResponse.md)
- [UpdateApprover](docs/Model/UpdateApprover.md)
- [UpdateApproverInfo](docs/Model/UpdateApproverInfo.md)
- [UpdateContact](docs/Model/UpdateContact.md)
- [UpdateCustomExperience](docs/Model/UpdateCustomExperience.md)
- [UpdateCustomExperienceRedirectUrls](docs/Model/UpdateCustomExperienceRedirectUrls.md)
- [UpdateDocument](docs/Model/UpdateDocument.md)
- [UpdateField](docs/Model/UpdateField.md)
- [UpdateFieldFont](docs/Model/UpdateFieldFont.md)
- [UpdateLabel](docs/Model/UpdateLabel.md)
- [UpdateSignatureRequest](docs/Model/UpdateSignatureRequest.md)
- [UpdateSignatureRequestReminderSettings](docs/Model/UpdateSignatureRequestReminderSettings.md)
- [UpdateSigner](docs/Model/UpdateSigner.md)
- [UpdateSignerConsentRequest](docs/Model/UpdateSignerConsentRequest.md)
- [UpdateSignerInfo](docs/Model/UpdateSignerInfo.md)
- [UpdateUser](docs/Model/UpdateUser.md)
- [UpdateWebhookSubscription](docs/Model/UpdateWebhookSubscription.md)
- [UpdateWorkspace](docs/Model/UpdateWorkspace.md)
- [User](docs/Model/User.md)
- [UserInvitation](docs/Model/UserInvitation.md)
- [UserRole](docs/Model/UserRole.md)
- [UserStatus](docs/Model/UserStatus.md)
- [UserWorkspacesInner](docs/Model/UserWorkspacesInner.md)
- [WatchlistFull](docs/Model/WatchlistFull.md)
- [WatchlistFullAllOfData](docs/Model/WatchlistFullAllOfData.md)
- [WatchlistFullAllOfDataPoliticallyExposedPerson](docs/Model/WatchlistFullAllOfDataPoliticallyExposedPerson.md)
- [WatchlistFullAllOfDataPoliticallyExposedPersonPositions](docs/Model/WatchlistFullAllOfDataPoliticallyExposedPersonPositions.md)
- [WatchlistFullAllOfDataPoliticallyExposedPersonSources](docs/Model/WatchlistFullAllOfDataPoliticallyExposedPersonSources.md)
- [WatchlistFullAllOfDataSanctions](docs/Model/WatchlistFullAllOfDataSanctions.md)
- [WatchlistFullAllOfDataSanctionsRecords](docs/Model/WatchlistFullAllOfDataSanctionsRecords.md)
- [WatchlistFullAllOfDataSanctionsSources](docs/Model/WatchlistFullAllOfDataSanctionsSources.md)
- [WatchlistMeta](docs/Model/WatchlistMeta.md)
- [WatchlistStatus](docs/Model/WatchlistStatus.md)
- [WebhookSubscription](docs/Model/WebhookSubscription.md)
- [WebhookSubscriptionScopes](docs/Model/WebhookSubscriptionScopes.md)
- [WebhookSubscriptionSubscribedEvents](docs/Model/WebhookSubscriptionSubscribedEvents.md)
- [WebhookSubscriptionWorkspaces](docs/Model/WebhookSubscriptionWorkspaces.md)
- [Workspace](docs/Model/Workspace.md)
- [WorkspaceUsersInner](docs/Model/WorkspaceUsersInner.md)

## Authorization

Authentication schemes defined for the API:
### bearerAuth

- **Type**: Bearer authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

contact@yousign.com

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `3.0`
    - Generator version: `7.15.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
