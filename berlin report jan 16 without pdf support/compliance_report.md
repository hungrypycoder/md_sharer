# Open Banking Compliance Analysis Report

**Report ID:** `f9e1eeca-7110-46e3-936e-698f10bbb420`  
**Generated:** January 16, 2026 at 02:41 UTC  
**Specification:** c11d1a51-22fa-4934-a589-afb65d38f081

---

## Executive Summary

| Metric | Value |
|--------|-------|
| Total Requirements Analyzed | **231** |
| Requirements with Gaps | **174** (75.3%) |
| Compliance Rate | **0.0%** |

### Support Level Breakdown

| Status | Count | Percentage |
|--------|-------|------------|
| Fully Supported | 0 | 0.0% |
| Partially Supported | 112 | 48.5% |
| Not Supported | 61 | 26.4% |
| Requires Configuration | 0 | 0.0% |
| Unknown | 1 | 0.4% |

### Dependency Analysis

| Property | Value |
|----------|-------|
| Total Dependencies | 0 |
| Graph Type | Valid DAG |
| Max Dependency Depth | 0 |
| Root Requirements | 231 |
| Leaf Requirements | 231 |

---

## Gap Analysis by Capability

<details>
<summary><strong>Account Information</strong> — 25 gap(s) | 7 not supported | 18 partial</summary>

### Account Information

*25 gap(s) identified*

#### GAP_0001: ATOM_191

**Requirement:** The GET /v1/card-accounts/{account-id}/transactions endpoint SHALL support dateFrom query parameter to specify the starting date of the transaction list.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. If this is not populated, the permissions will be open ended.All
              dates in the JSON payloads are represented in ISO 8601 date-time
              format.

              All date-time field...

2. For transaction entries subject to availability/float and for which
      availability information is provided, the value date must not be used. In
      this case the availability component identifie...

3. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

</details>

---

#### GAP_0004: ATOM_192

**Requirement:** The bookingStatus parameter SHALL be mandatory and support 'booked' status, with 'pending' and 'both' being optional for the ASPSP.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, specifically within the `wso2/financial-services-accelerator` project, supports the `bookingStatus` parameter with \'B...

</details>

---

#### GAP_0006: ATOM_160

**Requirement:** The system SHALL support Accept header for specifying preferred response formats including JSON, XML, and text/plain

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. If this is not populated, the permissions will be open ended.All
              dates in the JSON payloads are represented in ISO 8601 date-time
              format.

              All date-time field...

2. All dates in the HTTP headers are represented as RFC 7231 Full Dates. An
      example is below:

3. ### Authorize a consent

The bank sends the request to the customer stating the accounts and information that the API consumer wishes to access.
    
       
  1. Generate the request object by signin...

</details>

---

#### GAP_0025: ATOM_165

**Requirement:** Transaction responses MUST support both booked and pending transaction categories

- **Strength:** `MUST`
- **Section:** `f30dd2c91d5e`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. 2017-04-05T10:43:07+00:00
        type: string
        format: date-time
      InstructedAmount:
        type: object
        required:
          - Amount
          - Currency
        description: >-
...

2. If this is not populated, the permissions will be open ended.All
              dates in the JSON payloads are represented in ISO 8601 date-time
              format.

              All date-time field...

3. For transaction entries subject to availability/float and for which
      availability information is provided, the value date must not be used. In
      this case the availability component identifie...

</details>

---

#### GAP_0032: ATOM_166

**Requirement:** Standing orders MUST include standingOrderDetails with startDate, endDate, executionRule, and frequency

- **Strength:** `MUST`
- **Section:** `f30dd2c91d5e`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, `wso2/financial-services-accelerator`, appears to support standing orders with `startDate`, `endDate`, `executionRule`...

</details>

---

#### GAP_0045: ATOM_169

**Requirement:** Standing order information requests MUST use bookingStatus parameter with value 'information'

- **Strength:** `MUST`
- **Section:** `f30dd2c91d5e`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, `wso2/financial-services-accelerator`, appears to support standing order information requests, but the provided contex...

</details>

---

#### GAP_0052: ATOM_170

**Requirement:** The API MUST support a GET endpoint at /v1/accounts/{account-id}/transactions/{transactionId} to read transaction details for a specific transaction on a given account.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

2. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

3. If this is not populated, the permissions will be open ended.All
              dates in the JSON payloads are represented in ISO 8601 date-time
              format.

              All date-time field...

</details>

---

#### GAP_0060: ATOM_172

**Requirement:** The transactionId path parameter MUST be a string that corresponds to the transactionId attribute from a transaction list entry.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. 2017-04-05T10:43:07+00:00
        type: string
        format: date-time
      InstructedAmount:
        type: object
        required:
          - Amount
          - Currency
        description: >-
...

2. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

3. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

</details>

---

#### GAP_0080: ATOM_011

**Requirement:** When the underlying account is a multicurrency account, the first reference SHALL refer to the collection of all sub-accounts addressable by the IBAN, and the second reference SHALL refer to the euro sub-account only.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. 2017-04-05T10:43:07+00:00
        type: string
        format: date-time
      InstructedAmount:
        type: object
        required:
          - Amount
          - Currency
        description: >-
...

2. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

3. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

</details>

---

#### GAP_0087: ATOM_012

**Requirement:** The interface specification SHALL act on sub-accounts of multicurrency accounts in exactly the same way as on regular accounts for payment initiation and account information services.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. 2017-04-05T10:43:07+00:00
        type: string
        format: date-time
      InstructedAmount:
        type: object
        required:
          - Amount
          - Currency
        description: >-
...

2. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

3. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

</details>

---

#### GAP_0093: ATOM_148

**Requirement:** The system SHALL support multicurrency accounts by setting currency code to 'XXX' for aggregated multicurrency account views

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. 2017-04-05T10:43:07+00:00
        type: string
        format: date-time
      InstructedAmount:
        type: object
        required:
          - Amount
          - Currency
        description: >-
...

2. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

3. For transaction entries subject to availability/float and for which
      availability information is provided, the value date must not be used. In
      this case the availability component identifie...

</details>

---

#### GAP_0098: ATOM_149

**Requirement:** The system SHALL provide _links object with balances and transactions href URLs for each accessible account based on consent permissions

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

2. ### Retrieve a consent 
- An API consumer can retrieve a consent resource that they have created to check its status. In order to make this request, 
the API consumer must have an access token issued ...

3. ### Delete a consent
- If the customer revokes a consent to data access with the API consumer, the API consumer must delete the consent resource. 
In order to make this request, the API consumer must ...

</details>

---

#### GAP_0099: ATOM_180

**Requirement:** The API MUST support a GET endpoint at /v1/card-accounts to read a list of card accounts with additional information including balance information.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

2. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

3. ### Retrieve a consent 
- An API consumer can retrieve a consent resource that they have created to check its status. In order to make this request, 
the API consumer must have an access token issued ...

</details>

---

#### GAP_0103: ATOM_181

**Requirement:** The API MUST support a GET endpoint at /v1/card-accounts/{account-id} to read details about a specific card account.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

2. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

3. ### Retrieve a consent 
- An API consumer can retrieve a consent resource that they have created to check its status. In order to make this request, 
the API consumer must have an access token issued ...

</details>

---

#### GAP_0108: ATOM_152

**Requirement:** The system SHALL require X-Request-ID header as mandatory UUID for all account information requests

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ### Authorize a consent

The bank sends the request to the customer stating the accounts and information that the API consumer wishes to access.
    
       
  1. Generate the request object by signin...

2. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

3. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

</details>

---

#### GAP_0111: ATOM_183

**Requirement:** The card account list response MUST include a cardAccounts array containing Card Account Details objects.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

2. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

3. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

</details>

---

#### GAP_0116: ATOM_184

**Requirement:** The card account details response MUST include a cardAccount object containing Card Account Details.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

2. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

3. 2017-04-05T10:43:07+00:00
        type: string
        format: date-time
      InstructedAmount:
        type: object
        required:
          - Amount
          - Currency
        description: >-
...

</details>

---

#### GAP_0121: ATOM_185

**Requirement:** The GET /v1/card-accounts/{account-id}/balances endpoint SHALL return HTTP response code 200 on successful balance retrieval.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

2. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

3. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

</details>

---

#### GAP_0126: ATOM_155

**Requirement:** The GET /v1/accounts/{account-id}/balances endpoint SHALL return account balances with balanceAmount, balanceType, and reference date information

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

2. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

3. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

</details>

---

#### GAP_0134: ATOM_157

**Requirement:** The GET /v1/accounts/{account-id}/transactions endpoint SHALL support bookingStatus parameter with values 'booked', 'pending', 'both', and 'information'

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

2. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

3. For transaction entries subject to availability/float and for which
      availability information is provided, the value date must not be used. In
      this case the availability component identifie...

</details>

---

#### GAP_0138: ATOM_031

**Requirement:** The card-accounts endpoint MUST deliver credit card account related account information where the account is used to reconcile credit card transactions with the PSU

- **Strength:** `MUST`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

2. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

3. This document provides step by step instructions to tryout the flow with Manual Client Registration. This includes

- Setting up WSO2 FInancial Services Key Manager
- Create application using Manual C...

</details>

---

#### GAP_0144: ATOM_159

**Requirement:** The system MAY support delta access through entryReferenceFrom parameter or deltaList boolean flag

- **Strength:** `MAY`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, `wso2/financial-services-accelerator`, appears to support delta access for transactions through date-time parameters i...

</details>

---

#### GAP_0145: ATOM_032

**Requirement:** The GET card-accounts/{account-id}/transactions endpoint SHALL be mandatory for reading transaction lists related to a given card account

- **Strength:** `MANDATORY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

2. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

3. 2017-04-05T10:43:07+00:00
        type: string
        format: date-time
      InstructedAmount:
        type: object
        required:
          - Amount
          - Currency
        description: >-
...

</details>

---

#### GAP_0147: ATOM_193

**Requirement:** The ASPSP MAY support deltaList parameter to indicate that the AISP wants all transactions after the last report access for the PSU on the addressed account.

- **Strength:** `MAY`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

2. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': "This repository, `wso2/financial-services-accelerator`, does not explicitly support a `deltaList` parameter for transactions. The provi...

</details>

---

#### GAP_0165: ATOM_151

**Requirement:** The system MAY include booking balance in account details when withBalance query parameter is true and PSU consent permits balance access

- **Strength:** `MAY`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. Note, the account name is not the product name or the nickname of the
      account.
    type: string
    minLength: 1
    maxLength: 70
  SecondaryIdentification:
    description: >-
      This is se...

2. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

3. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

</details>

---

</details>

<details>
<summary><strong>Authentication</strong> — 43 gap(s) | 17 not supported | 26 partial</summary>

### Authentication

*43 gap(s) identified*

#### GAP_0003: ATOM_223

**Requirement:** ASPSP SHALL provide TPPs with configuration data conforming to the OAuth 2.0 Authorisation Server Metadata specification

- **Strength:** `SHALL`
- **Section:** `13`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

2. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

3. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

</details>

---

#### GAP_0007: ATOM_101

**Requirement:** ASPSPs MUST support selection of SCA authentication method by PSU when multiple methods are available

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

2. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

3. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

</details>

---

#### GAP_0008: ATOM_096

**Requirement:** ASPSPs MUST validate TPP role semantics for payment initiation requests

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

3. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

</details>

---

#### GAP_0009: ATOM_224

**Requirement:** client_id parameter SHALL contain organizationIdentifier as provided in the eIDAS certificate with specific structure format

- **Strength:** `SHALL`
- **Section:** `13.1`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### getKeyId method

The method contains the KeyID calculation logic. You can customize it according to your requirements. Given below is 
the method signature:

``` java
public String getKeyId(Certif...

2. ## Client Creation

The OpenAPI extension for dynamic client creation  provides the extendibility to validate the incoming dynamic client registration request attributes and store custom client data a...

3. ## Writing a custom ID Token Builder

The default ID Token Builder in WSO2 Open Banking provides the pairwise subject calculation for authorization and token 
flow.

If the API consumer application su...

</details>

---

#### GAP_0013: ATOM_102

**Requirement:** ASPSPs MUST return ASPSP-SCA-Approach header with value DECOUPLED when branching to Decoupled SCA Approach

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

2. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

3. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

</details>

---

#### GAP_0014: ATOM_225

**Requirement:** scope parameter SHALL reference the payment or consent resource in the format "PIS:<paymentId>", "AIS:<consentId>", or "PIIS:<consentId>"

- **Strength:** `SHALL`
- **Section:** `13.1`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Step 2: Initiate a consent

In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. 

A sample consent initia...

2. ## Consent Authorization

- Once you enter a properly constructed authorization request in your web browser, based on the `bank_code` in the 
  request object, you will be redirected to ABC bank or DC...

3. During the consent authorization process, the banks redirect customers to provide consent for API consumers to access their banking information. The process is as follows: 1. API consumer requests to ...

</details>

---

#### GAP_0016: ATOM_195

**Requirement:** The POST /v1/{payment-service}/{payment-product}/{paymentId}/authorisations endpoint SHALL create an authorisation sub-resource and return HTTP response code 201.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

2. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

3. reference: ``` [open_banking.push_authorisation] expiry_time=60 request_uri_sub_string="substring" ``` !!! note You can change the format of the request_uri using the `request_uri_sub_string` tag. ```...

</details>

---

#### GAP_0019: ATOM_119

**Requirement:** The Authorization header SHALL be included only if OAuth2 based authentication was performed in a pre-step or SCA was performed

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### setConditionalAuthScript method
This method lets you set a [conditional authentication script](https://is.docs.wso2.com/en/5.11.0/learn/using-opa-policies-for-adaptive-auth/#configure-the-adaptive...

2. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

3. ## Client Authentication 

According to OAuth 2.0, the authorization server and the client need to establish a client authentication method that 
meets the security requirements of the authorization s...

</details>

---

#### GAP_0020: ATOM_088

**Requirement:** ASPSP must validate Client ID, Redirect URI, and TPP Role when using OAuth2 SCA approach

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

2. ## Client Authentication 

According to OAuth 2.0, the authorization server and the client need to establish a client authentication method that 
meets the security requirements of the authorization s...

3. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

</details>

---

#### GAP_0022: ATOM_196

**Requirement:** The authorisationId field SHALL be mandatory in the response and contain a unique resource identification of the created authorisation sub-resource.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. | MsgInfoDTO | resource | String | An API resource | | ResponseContextDTO | MsgInfoDTO | electedResource | String | An elected resource | | ResponseContextDTO | MsgInfoDTO | httpMethod | String | The ...

2. ##Writing a Custom Request Object Validator
A Request Object contains authentication and authorization request parameters in a self-contained JWT. It is used in the 
authorization endpoint of WSO2 Ide...

3. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

</details>

---

#### GAP_0024: ATOM_228

**Requirement:** TPP SHALL be authenticated during token request using OAuth 2.0 Mutual TLS Client Authentication and Certificate Bound Access Tokens in conjunction with the TPP's eIDAS certificate

- **Strength:** `SHALL`
- **Section:** `13.3`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Grant Handler

A Grant Handler validates the grant, scopes, and access delegation. By default, the following Grant Handler types are 
engaged when issuing tokens:

   - Authorization Code Grant Ha...

2. ## Client Authentication 

According to OAuth 2.0, the authorization server and the client need to establish a client authentication method that 
meets the security requirements of the authorization s...

3. ### Step 5: Generate keys

The TPP application requires a Client ID (Consumer Key) to access the subscribed API.

1. Go to the **Applications** tab in the Developer Portal.

2. From the application li...

</details>

---

#### GAP_0028: ATOM_197

**Requirement:** The scaStatus field SHALL be mandatory in the authorisation response to indicate the current status of the SCA process.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ## Validate Authorize Request

The OpenAPI extension for validate client sending authorize API requests to ensure request parameters are according to  the way
allowed in the Open Banking  specificatio...

2. A pushed authorization request contains authentication and authorization request parameters, which will be used in the Pushed Authorization endpoint of WSO2 Open Banking Accelerator. The Pushed Author...

3. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

</details>

---

#### GAP_0034: ATOM_198

**Requirement:** The TPP-Redirect-URI header SHALL be mandatory for the Redirect SCA Approach when TPP-Redirect-Preferred equals true.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Step 2: Sign in to the Developer Portal as the TPP

1. Now, sign in to the [Developer portal](https://<APIM_HOST>:9443/devportal) as the TPP.

2. Enter the username and the password you entered wh...

2. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

3. ### Step 1: Sign up as a TPP

1. Go to the Developer portal at `https://<APIM_HOST>:9443/devportal`.

2. Go to the **Applications** tab. <br/> ![applications_tab](../../assets/img/learn/mcr/applicatio...

</details>

---

#### GAP_0041: ATOM_110

**Requirement:** The Authorization header SHALL be included only if OAuth2 based authentication was performed in a pre-step or OAuth2 based SCA was performed in current PIS transaction or preceding AIS service in same session

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Step 5: Invoking Accounts and Transaction API

Once the user approves the account consent, the TPP is eligible to access the account details of the user.

The TPP can now invoke the GET/ accounts ...

2. ### Step 2: Initiate a consent

In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. 

A sample consent initia...

3. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

</details>

---

#### GAP_0042: ATOM_200

**Requirement:** TPP SHALL create a one-time use XSRF token to be conveyed to the ASPSP in the state parameter when preparing an authorization request in Redirect SCA approach.

- **Strength:** `SHALL`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

2. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

3. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

</details>

---

#### GAP_0044: ATOM_100

**Requirement:** ASPSPs MUST provide available SCA methods to PSU when multiple authentication methods are supported

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

2. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

3. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

</details>

---

#### GAP_0046: ATOM_129

**Requirement:** The ASPSP shall perform Strong Customer Authentication (SCA) as mandated by EBA-RTS for consent authorization

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

2. ## How to manage consents

The API consumer applications seek consent from their customers who wish to expose their financial data through the 
application. When granting consent the customers must kn...

3. #Client-Initiated Backchannel Authentication (CIBA) Flow

WSO2 Open Banking Accelerator provides support for the
[OpenID Connect Client-Initiated Backchannel Authentication Flow](https://openid.net/sp...

</details>

---

#### GAP_0049: ATOM_201

**Requirement:** TPP SHALL bind the XSRF token value to the current session in the user agent when preparing authorization request.

- **Strength:** `SHALL`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Step 5: Generate keys

The TPP application requires a Client ID (Consumer Key) to access the subscribed API.

1. Go to the **Applications** tab in the Developer Portal.

2. From the application li...

2. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

3. ### Step 5: Invoking Accounts and Transaction API

Once the user approves the account consent, the TPP is eligible to access the account details of the user.

The TPP can now invoke the GET/ accounts ...

</details>

---

#### GAP_0050: ATOM_202

**Requirement:** TPP MUST generate a nonce for the challenge parameter in addition to XSRF token when using integrated OAuth SCA Approach.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Step 5: Generate keys

The TPP application requires a Client ID (Consumer Key) to access the subscribed API.

1. Go to the **Applications** tab in the Developer Portal.

2. From the application li...

2. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

3. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

</details>

---

#### GAP_0053: ATOM_014

**Requirement:** The API SHALL support multiple level SCA where a transaction needs authorisation by more than one PSU in a corporate context.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ISO 20022). - mediation between a legacy or digital core and other banking systems, and the bank’s library of open banking APIs. 6. **Data Analytics** - The solution to mediate between the bank’s syst...

2. ## Stakeholders in Open Banking / Open Finance
   
The open banking ecosystem comprises 4 main stakeholders.
   
   * **Customer** - The owner of a bank account who can grant access to the API consume...

3. # Financial -grade API (FAPI) Security

Financial-grade API (FAPI), a specification that extends the OAuth and OIDC frameworks, 
was introduced by the FAPI Working Group and defines additional technic...

</details>

---

#### GAP_0056: ATOM_065

**Requirement:** The system shall provide SCA process status information through scaStatus data element in GET SCA Status Response Message for payment initiation

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. backendTime)`|`142`| In addition to the above-mentioned data elements, you can publish data that are specific to your open banking standard. For information on the additional data elements that you ca...

3. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

</details>

---

#### GAP_0058: ATOM_203

**Requirement:** TPP MUST check whether the state parameter is linked to the current session when retrieving GET command from PSU browser.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

2. ### Step 5: Invoking Accounts and Transaction API

Once the user approves the account consent, the TPP is eligible to access the account details of the user.

The TPP can now invoke the GET/ accounts ...

3. ### Step 1: Sign up as a TPP

1. Go to the Developer portal at `https://<APIM_HOST>:9443/devportal`.

2. Go to the **Applications** tab. <br/> ![applications_tab](../../assets/img/learn/mcr/applicatio...

</details>

---

#### GAP_0059: ATOM_093

**Requirement:** PSU must authenticate with first factor before account or SCA method details are available to PISP in embedded SCA approach

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

2. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

3. ## Configuring a custom Push Authenticator  

1. Once implemented, build a JAR file for your project.
2. Place the above-created JAR file in the `<IS_HOME>/repository/components/dropins` directory.
3....

</details>

---

#### GAP_0061: ATOM_067

**Requirement:** The system shall set transaction status to PATC (PartiallyAcceptedTechnicalCorrect) for payments authorized by at least one PSU but not yet fully authorized in multilevel SCA processes

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

3. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

</details>

---

#### GAP_0062: ATOM_204

**Requirement:** TPP MUST stop the transaction if the state parameter validation check fails.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

2. A pushed authorization request contains authentication and authorization request parameters, which will be used in the Pushed Authorization endpoint of WSO2 Open Banking Accelerator. The Pushed Author...

3. ### Step 5: Invoking Accounts and Transaction API

Once the user approves the account consent, the TPP is eligible to access the account details of the user.

The TPP can now invoke the GET/ accounts ...

</details>

---

#### GAP_0063: ATOM_099

**Requirement:** ASPSPs MUST support one-time password (OTP) authentication method in Embedded SCA Approach

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### setConditionalAuthScript method
This method lets you set a [conditional authentication script](https://is.docs.wso2.com/en/5.11.0/learn/using-opa-policies-for-adaptive-auth/#configure-the-adaptive...

2. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

3. ### setAuthenticators method
This method lets you configure authenticators to be invoked during the authorization flow.

``` java
public void setAuthenticators (boolean isRegulatoryApp, String tenantD...

</details>

---

#### GAP_0065: ATOM_021

**Requirement:** ASPSPs SHALL enable direct start of Redirect SCA processing after payment or consent submission if no other data from the TPP has to be submitted.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

2. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

3. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

</details>

---

#### GAP_0081: ATOM_020

**Requirement:** The signing basket SHALL get the status of being fully authorised as soon as all grouped transactions have been successfully authorised by the applied SCA mechanism.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Consent Authorization

- Once you enter a properly constructed authorization request in your web browser, based on the `bank_code` in the 
  request object, you will be redirected to ABC bank or DC...

2. ## How WSO2 Open Banking Accelerator delivers open banking requirements 1. **API Consumer Onboarding** - API consumer onboarding is the process of verifying an API consumer when they register with a b...

3. ### Java based extensions (Old approach)

   - [Open Banking Service Activator](service-activator.md)
   - [Consent Management](consent-management-manage.md)
   - [Token Flow Customization](jwt-access...

</details>

---

#### GAP_0082: ATOM_016

**Requirement:** The API SHALL support signing of a group of transactions with multi-level SCA where the group needs authorisation by more than one PSU in a corporate context.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ISO 20022). - mediation between a legacy or digital core and other banking systems, and the bank’s library of open banking APIs. 6. **Data Analytics** - The solution to mediate between the bank’s syst...

2. ## How WSO2 Open Banking Accelerator delivers open banking requirements 1. **API Consumer Onboarding** - API consumer onboarding is the process of verifying an API consumer when they register with a b...

3. ## Stakeholders in Open Banking / Open Finance
   
The open banking ecosystem comprises 4 main stakeholders.
   
   * **Customer** - The owner of a bank account who can grant access to the API consume...

</details>

---

#### GAP_0092: ATOM_008

**Requirement:** XS2A API must support OAuth2 Authorization Code Grant flow for payment authorization using scope attribute to refer to payment data

- **Strength:** `MUST`
- **Section:** `eef9ab97432c - 4.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## Create API resources

WSO2 Identity Server provides comprehensive capabilities for managing and securing API resources, particularly in the context of authorization and access control. You need to ...

2. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

3. ### Step 2: Initiate a consent

In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. 

A sample consent initia...

</details>

---

#### GAP_0096: ATOM_013

**Requirement:** The NextGenPSD2 API SHALL support dedicated authorisation endpoints for payment initiation transactions and establish consent transactions to handle transaction authorisation by PSUs.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## How WSO2 Open Banking Accelerator delivers open banking requirements 1. **API Consumer Onboarding** - API consumer onboarding is the process of verifying an API consumer when they register with a b...

2. ## What is new in this release

####WSO2 Open Banking Accelerator for Identity Server 

- Accelerator-level support for both pre-initiated and scope-based consent flows
- OpenAPI based accelerator ext...

3. ### push-auth/authenticate endpoint

The SDK invokes the `push-auth/authenticate` endpoint within the `sendAuthRequest()` method to send the consent 
authorization status (approved/denied) to the auth...

</details>

---

#### GAP_0119: ATOM_123

**Requirement:** The TPP-Redirect-URI header SHALL be mandatory for the Redirect SCA Approach when TPP-Redirect-Preferred equals true

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

2. ### Step 2: Sign in to the Developer Portal as the TPP

1. Now, sign in to the [Developer portal](https://<APIM_HOST>:9443/devportal) as the TPP.

2. Enter the username and the password you entered wh...

3. ### Step 1: Sign up as a TPP

1. Go to the Developer portal at `https://<APIM_HOST>:9443/devportal`.

2. Go to the **Applications** tab. <br/> ![applications_tab](../../assets/img/learn/mcr/applicatio...

</details>

---

#### GAP_0120: ATOM_026

**Requirement:** TPPs SHALL be identified by PSD2 related eIDAS certificates as mandated by PSD2.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

2. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

3. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

</details>

---

#### GAP_0125: ATOM_015

**Requirement:** The API SHALL support signing of a group of transactions with one SCA as offered by ASPSPs in online banking.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ISO 20022). - mediation between a legacy or digital core and other banking systems, and the bank’s library of open banking APIs. 6. **Data Analytics** - The solution to mediate between the bank’s syst...

2. ## Stakeholders in Open Banking / Open Finance
   
The open banking ecosystem comprises 4 main stakeholders.
   
   * **Customer** - The owner of a bank account who can grant access to the API consume...

3. reference: ``` [open_banking.push_authorisation] expiry_time=60 request_uri_sub_string="substring" ``` !!! note You can change the format of the request_uri using the `request_uri_sub_string` tag. ```...

</details>

---

#### GAP_0129: ATOM_017

**Requirement:** Payment resources that need to be signed n times SHALL end up with n SCA sub-resources in a normal successful process.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

3. ## Create API resources

WSO2 Identity Server provides comprehensive capabilities for managing and securing API resources, particularly in the context of authorization and access control. You need to ...

</details>

---

#### GAP_0137: ATOM_220

**Requirement:** TPP SHALL include the TPP-Signature-Certificate header containing the TPP's eIDAS certificate when making authenticated requests

- **Strength:** `SHALL`
- **Section:** `4e52743eb3ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

2. ### Step 5: Invoking Accounts and Transaction API

Once the user approves the account consent, the TPP is eligible to access the account details of the user.

The TPP can now invoke the GET/ accounts ...

3. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

</details>

---

#### GAP_0139: ATOM_189

**Requirement:** The Authorization header field SHALL only be contained if an OAuth2 based authentication was performed in a pre-step or an OAuth2 based SCA was performed in the related consent authorisation.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. During the consent authorization process, the banks redirect customers to provide consent for API consumers to access their banking information. The process is as follows: 1. API consumer requests to ...

2. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

3. ### Step 5: Validate Account Information Invocation

The Consent Validate implements the validations that are required when the resource endpoints are invoked with a user access token.

!!! note
    I...

</details>

---

#### GAP_0141: ATOM_103

**Requirement:** ASPSPs MUST support multilevel SCA approach with explicit start of multiple authorisation mechanisms

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

2. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

3. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

</details>

---

#### GAP_0146: ATOM_027

**Requirement:** TPP brand names MAY be entered into the certificate field Organisation Unit (OU) and ASPSPs MAY ignore entries in this field.

- **Strength:** `MAY`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

2. components:
  parameters:
    consentId:
      name: "consentId"
      in: "path"
      description: "ConsentId"
      required: true
      schema:
        type: "string"
    authorization:
      in: ...

3. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

</details>

---

#### GAP_0160: ATOM_176

**Requirement:** The Authorization header SHOULD be included when OAuth2 based authentication was performed in a pre-step or OAuth2 based SCA was performed in the related consent authorization.

- **Strength:** `SHOULD`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. During the consent authorization process, the banks redirect customers to provide consent for API consumers to access their banking information. The process is as follows: 1. API consumer requests to ...

2. ### push-auth/authenticate endpoint

The SDK invokes the `push-auth/authenticate` endpoint within the `sendAuthRequest()` method to send the consent 
authorization status (approved/denied) to the auth...

3. ### Step 2: Initiate a consent

In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. 

A sample consent initia...

</details>

---

#### GAP_0170: ATOM_018

**Requirement:** ASPSPs MAY offer the signing-baskets endpoint to support grouping several transactions for one common authorisation process.

- **Strength:** `MAY`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

2. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

3. ## Java based extensions (Old approach)

- [Open Banking Gateway](open-banking-gateway.md)
- [Open Banking Event Executor](custom-event-executor.md)
- [Data Publishing](authentication-flow-for-data-pu...

</details>

---

#### GAP_0172: ATOM_221

**Requirement:** OAuth2 response type "code" and grant types "authorization_code" and "refresh_token" SHOULD be used

- **Strength:** `SHOULD`
- **Section:** `13`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## User Access Token

We need to obtain an access token from the retrieved access token. For that we are using `authorization_code` grant type 
as follows:

!!! tip
    You must send the registered tr...

2. ##Writing a Custom Response Type Handler

The Response Type handler contains an extension. According to your requirements, you can extend and override the methods 
in the `OBResponseTypeHandler` class...

3. # supported types : Basic-Auth or OAuth2
type = "Basic-Auth"
username = ""
password = ""
```

</details>

---

#### GAP_0173: ATOM_019

**Requirement:** When offering the signing basket function, ASPSPs MAY restrict the grouping to specific types such as payments only, individual payments, or the same payment product.

- **Strength:** `MAY`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

3. ### Account Information Service

If the API consumer application is aggregating account information on behalf of the bank user, the APP-to-APP redirection 
flow is as follows: 

[ ![](../assets/img/le...

</details>

---

</details>

<details>
<summary><strong>Certificate Management</strong> — 9 gap(s) | 3 not supported | 6 partial</summary>

### Certificate Management

*9 gap(s) identified*

#### GAP_0037: ATOM_095

**Requirement:** ASPSPs MUST validate eIDAS certificate request syntax for payment initiation requests

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to have some capabilities related to certificate validation and authorization details that could be relevant to...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support certificate validation, including mutual SSL, which could be relevant to validating eIDAS certif...

</details>

---

#### GAP_0077: ATOM_207

**Requirement:** TPP SHALL provide certificate used for signing the request in base64 encoding when signature is included.

- **Strength:** `SHALL`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the inclusion of a base64 encoded certificate in the `TPP-Signature-Certificate` header when a signature is pr...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support the provision of a base64 encoded certificate in a request header, specifically for mutual SSL a...

</details>

---

#### GAP_0088: ATOM_002

**Requirement:** TPP must use a qualified certificate for website authentication issued by a qualified trust service provider according to eIDAS regulation

- **Strength:** `MUST`
- **Section:** `eef9ab97432c - 4.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support X.509 certificate authentication, which is a foundational element for implementing eIDAS-compliant w...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support client certificate authentication, which is a prerequisite for using qualified certificates for ...

</details>

---

#### GAP_0090: ATOM_084

**Requirement:** TPP must validate eIDAS certificate, request syntax, TPP role, and semantics when receiving payment status response

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support aspects of certificate validation and API security that could be relevant to eIDAS certificate valid...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support client certificate management, which could be relevant to eIDAS certificate validation, and also...

</details>

---

#### GAP_0104: ATOM_003

**Requirement:** TPP certificate must be compliant with EBA-RTS requirements and indicate all roles the TPP is authorised to use

- **Strength:** `MUST`
- **Section:** `eef9ab97432c - 4.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, WSO2 Identity Server, appears to have some support for certificate validation, including the ability to check for invalid certificate cont...

2. [wso2/product-apim]
[{'type': 'text', 'text': "This repository, `wso2/product-apim`, appears to provide API endpoints for managing client and endpoint certificates, but it does not contain explicit im...

</details>

---

#### GAP_0106: ATOM_213

**Requirement:** The keyId field in the Signature header must contain the serial number of the TPP's certificate formatted as keyId="SN=XXX,CA=YYYYYYYYYYYYYYYY"

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the use of certificate serial numbers and CA distinguished names in the `keyId` field of a `Signatur...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support the use of certificate serial numbers and issuer distinguished names in security policies, which...

</details>

---

#### GAP_0115: ATOM_077

**Requirement:** The system shall validate eIDAS certificates in payment initiation requests

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support eIDAS certificate validation, particularly in the context of payment initiation requests. The system...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports certificate validation, including certificate chain validation and revocation checks, which are crucial fo...

</details>

---

#### GAP_0122: ATOM_006

**Requirement:** Electronic signature of TPP must be based on a qualified certificate for electronic seals issued by eIDAS-compliant qualified trust service provider

- **Strength:** `MUST`
- **Section:** `eef9ab97432c - 4.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not directly support the specific requirement of verifying that a TPP (Third Party Provider) signing certificate i...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not appear to directly support the specific requirement of verifying a TPP signing certificate based on a qual...

</details>

---

#### GAP_0143: ATOM_082

**Requirement:** The ASPSP SHALL validate eIDAS certificate request syntax, TPP role, and semantics during payment initiation

- **Strength:** `SHALL`
- **Section:** `648825991d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to have capabilities related to certificate handling and API security, which could be relevant to eIDAS certifi...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, this repository, `wso2/product-apim`, appears to handle the management of client and endpoint certificates, but ther...

</details>

---

</details>

<details>
<summary><strong>Consent Management</strong> — 18 gap(s) | 2 not supported | 15 partial | 1 unknown</summary>

### Consent Management

*18 gap(s) identified*

#### GAP_0027: ATOM_140

**Requirement:** The ASPSP shall support Global Consent model where TPP submits only PSU identification for global consent authorization

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Data
The following table explains the data available in `ConsentValidateData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| headers ...

2. ## Setting up Consent manager app

3. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

</details>

---

#### GAP_0035: ATOM_141

**Requirement:** The ASPSP shall display general account access information to PSU during SCA for Global Consent model

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Data 
The following table explains the data available in `ConsentRetrieveData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| session...

2. ### Data
The following table explains the data available in `ConsentValidateData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| headers ...

3. ### getConsentAmendmentHistoryData method

!!! info
    This is only available as a WSO2 Update from **WSO2 Open Banking Identity Server Accelerator Level
    3.0.0.33** onwards. For more information ...

</details>

---

#### GAP_0036: ATOM_126

**Requirement:** The ASPSP shall support Account Information Service consent with specified type of service to grant access to

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. #### Add CustomerCareOfficerRole Role

CustomerCareOfficerRole is required for bank users to log into the Consent Manager Portal and search for the consents granted by any user.

1. Go to **Roles** un...

2. ## Using Consent Manager

1. Go to the Consent Manager application at `https://<IS_HOST>:9446/consentmgr`.

2. Sign in with the credentials of the users created in [Create Users](../learn/consent-mana...

3. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

</details>

---

#### GAP_0047: ATOM_130

**Requirement:** The ASPSP shall create a consent resource with detailed access rights, validity status, and Consent-ID token upon successful authorization

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

2. ### createConsentAuthorization method
      
This method lets you create an authorization resource for a consent.
    
```java
AuthorizationResource createConsentAuthorization(AuthorizationResource au...

3. ### Data 
The following table explains the data available in `ConsentRetrieveData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| session...

</details>

---

#### GAP_0072: ATOM_175

**Requirement:** The Consent-ID header MUST be included to identify the corresponding consent granted by the PSU.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### getDetailedConsent method
 
This method lets you retrieve detailed consent for a given consent ID. A detailed consent includes the following in 
addition to consent resource-specific data: 

 - Re...

2. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

3. ### Data
The following table explains the data available in `ConsentValidateData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| headers ...

</details>

---

#### GAP_0075: ATOM_069

**Requirement:** The system shall support consent status 'expired' when consent has exceeded its validity period such as after 90 days

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### amendConsentData method

This method lets you amend the consent receipt or validity period. It is mandatory to provide the consent ID with 
either the consent receipt or validity period. When the ...

2. ### createExclusiveConsent method

This method lets you create an exclusive consent by performing the following:

 - Updates existing consent statuses and deactivate their account mappings
 - Creates ...

3. ## Using Consent Manager

1. Go to the Consent Manager application at `https://<IS_HOST>:9446/consentmgr`.

2. Sign in with the credentials of the users created in [Create Users](../learn/consent-mana...

</details>

---

#### GAP_0078: ATOM_146

**Requirement:** The ASPSP shall offer consent extension for both Detailed and Global Consent models if offered for one model

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** unknown
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## Setting up Consent manager app

2. ### Data model

The following table explains the data model associated with `ConsentHistoryResource`.

??? tip "Click here to see the data model associated with `ConsentHistoryResource`."
            ...

3. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

</details>

---

#### GAP_0079: ATOM_127

**Requirement:** The ASPSP shall support Account Information Service consent with multiplicity specification for one-off or recurring access

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. #### Add CustomerCareOfficerRole Role

CustomerCareOfficerRole is required for bank users to log into the Consent Manager Portal and search for the consents granted by any user.

1. Go to **Roles** un...

2. ### Data 
The following table explains the data available in `ConsentRetrieveData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| session...

3. ### amendConsentData method

This method lets you amend the consent receipt or validity period. It is mandatory to provide the consent ID with 
either the consent receipt or validity period. When the ...

</details>

---

#### GAP_0086: ATOM_068

**Requirement:** The system shall support consent status values 'received', 'rejected', and 'valid' during the AIS consent initiation phase

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

2. ### getConsent method

This method lets you retrieve a consent with or without its attributes by performing the following: 

- Retrieves the consent for status validation
- Optionally retrieves consen...

3. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

</details>

---

#### GAP_0107: ATOM_182

**Requirement:** Card account access MUST assume that PSU consent is already given and stored on the ASPSP system.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ## Using Consent Manager

1. Go to the Consent Manager application at `https://<IS_HOST>:9446/consentmgr`.

2. Sign in with the credentials of the users created in [Create Users](../learn/consent-mana...

2. #### Add CustomerCareOfficerRole Role

CustomerCareOfficerRole is required for bank users to log into the Consent Manager Portal and search for the consents granted by any user.

1. Go to **Roles** un...

3. ## Shareable and payable accounts 
   
Some bank customers may have a certain number of bank accounts in a particular bank, but not all these accounts have 
the ability to be shared externally or to m...

</details>

---

#### GAP_0110: ATOM_153

**Requirement:** The system SHALL require Consent-ID header as mandatory for account information requests

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

2. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

3. ### Data 
The following table explains the data available in `ConsentRetrieveData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| session...

</details>

---

#### GAP_0118: ATOM_071

**Requirement:** The system shall support consent status 'terminatedByTpp' when AIS has terminated the consent

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### createExclusiveConsent method

This method lets you create an exclusive consent by performing the following:

 - Updates existing consent statuses and deactivate their account mappings
 - Creates ...

2. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

3. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

</details>

---

#### GAP_0128: ATOM_186

**Requirement:** The account-id parameter SHALL be constant at least throughout the lifecycle of a given consent.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Persist

The second endpoint of the Consent Authorize component is the Persist Flow. The Persistent Steps are engaged once the 
user approves/denies the consent via an API invocation made from the ...

2. ### amendConsentData method

This method lets you amend the consent receipt or validity period. It is mandatory to provide the consent ID with 
either the consent receipt or validity period. When the ...

3. ### Data 
The following table explains the data available in `ConsentRetrieveData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| session...

</details>

---

#### GAP_0135: ATOM_070

**Requirement:** The system shall support consent status 'revokedByPsu' when consent has been revoked by the Payment Service User

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## Using Consent Manager

1. Go to the Consent Manager application at `https://<IS_HOST>:9446/consentmgr`.

2. Sign in with the credentials of the users created in [Create Users](../learn/consent-mana...

2. ### revokeConsent method

This method lets you revoke a consent by performing the following: 

 - Retrieves the consent for status validation
 - Updates the existing status of the consent
 - Creates a...

3. ### amendConsentData method

This method lets you amend the consent receipt or validity period. It is mandatory to provide the consent ID with 
either the consent receipt or validity period. When the ...

</details>

---

#### GAP_0136: ATOM_188

**Requirement:** The Consent-ID header field SHALL be mandatory and contain identification of the corresponding consent as granted by the PSU.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### getDetailedConsent method
 
This method lets you retrieve detailed consent for a given consent ID. A detailed consent includes the following in 
addition to consent resource-specific data: 

 - Re...

2. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

3. ### Data
The following table explains the data available in `ConsentValidateData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| headers ...

</details>

---

#### GAP_0161: ATOM_145

**Requirement:** The ASPSP may require explicit consent extension by PSU to deliver account owner name

- **Strength:** `MAY`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. #### Add ConsentPortalRole Role

ConsentPortalRole is required for users to log into the Consent Manager Portal and search for the consents granted by them.

Similarly create another role named as **C...

2. #### Add CustomerCareOfficerRole Role

CustomerCareOfficerRole is required for bank users to log into the Consent Manager Portal and search for the consents granted by any user.

1. Go to **Roles** un...

3. ## Using Consent Manager

1. Go to the Consent Manager application at `https://<IS_HOST>:9446/consentmgr`.

2. Sign in with the credentials of the users created in [Create Users](../learn/consent-mana...

</details>

---

#### GAP_0162: ATOM_035

**Requirement:** The GET consents/{consentId} endpoint SHALL be mandatory for reading the exact definition of a given consent resource including validity status

- **Strength:** `MANDATORY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### getDetailedConsent method
 
This method lets you retrieve detailed consent for a given consent ID. A detailed consent includes the following in 
addition to consent resource-specific data: 

 - Re...

2. ### getConsent method

This method lets you retrieve a consent with or without its attributes by performing the following: 

- Retrieves the consent for status validation
- Optionally retrieves consen...

3. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

</details>

---

#### GAP_0168: ATOM_036

**Requirement:** The DELETE consents/{consentId} endpoint SHALL be mandatory for terminating the addressed consent

- **Strength:** `MANDATORY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## **Usage** **>> consent-cleanup.sql** This is a consent data cleanup script with batch wise delete, This procedure includes the cleanup of consents from the respective tables of *FS_CONSENT* , *FS_C...

2. ### deleteConsentAttributes method

This method lets you delete a provided list of consent attributes for a particular consent.

``` java
boolean deleteConsentAttributes(String consentID, ArrayList<St...

3. ### revokeExistingApplicableConsents method

This method lets you revoke existing consents for a given combination of `clientID`, `userID`, `consent type`, and 
`status` parameters. It also revokes an...

</details>

---

</details>

<details>
<summary><strong>Data Access</strong> — 8 gap(s) | 1 not supported | 7 partial</summary>

### Data Access

*8 gap(s) identified*

#### GAP_0010: ATOM_134

**Requirement:** The ASPSP shall deny access for one-off consent if AISP requests data more than once or validity has timed out

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports denying access for one-off consents if the AISP requests data more than once or if the validity has timed out....

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports denying access based on request counts and time periods, which can be configured to enforce one-off consen...

</details>

---

#### GAP_0012: ATOM_137

**Requirement:** The ASPSP shall check access frequency per account and per PSU for consents covering multiple accounts

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support consent management, which is a prerequisite for tracking access frequency per account and per PSU fo...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, WSO2 API Manager, supports rate limiting and throttling policies that can be configured to control API usage. While the provided snippet...

</details>

---

#### GAP_0023: ATOM_135

**Requirement:** The ASPSP shall deny data access if requested service type does not comply with consented service

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Yes, the WSO2 Identity Server repository supports denying data access if the requested service type does not comply with consented services through its Con...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports denying data access based on service type not complying with consented service through its deny policy fea...

</details>

---

#### GAP_0064: ATOM_132

**Requirement:** The ASPSP shall validate Read Account Data Request against PSU consent for type of account data to be accessed

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the validation of "Read Account Data Request" against "PSU consent for type of account data to be accessed" th...

2. [wso2/product-apim]
[{'type': 'text', 'text': "This repository, `wso2/product-apim`, appears to support the validation of Read Account Data Requests against PSU (Payment Services User) consent for the...

</details>

---

#### GAP_0070: ATOM_133

**Requirement:** The ASPSP shall validate Read Account Data Request against PSU consent for addressed account identification where applicable

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the validation of "Read Account Data Request" against "PSU consent for addressed account identification" throu...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, includes features related to consent management, which could be relevant to validating account data requests agains...

</details>

---

#### GAP_0071: ATOM_143

**Requirement:** The ASPSP shall make detailed consent information retrievable by TPP via GET consent object for Bank Offered Consent

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the retrieval of detailed consent information by a TPP (Third Party Provider) via a GET consent object, which ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support consent management, which is a prerequisite for retrieving consent information. The presence of ...

</details>

---

#### GAP_0124: ATOM_154

**Requirement:** The system SHALL include PSU-IP-Address header when request was actively initiated by PSU

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, WSO2 Identity Server, appears to have mechanisms for handling and potentially manipulating IP addresses in HTTP requests, but there is no ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to handle IP addresses for security and analytical purposes, but there is no direct evidence of a "PSU-IP-A...

</details>

---

#### GAP_0140: ATOM_136

**Requirement:** The ASPSP shall deny data access if actual access does not match consented duration or frequency

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports consent management, which is a prerequisite for enforcing data access based on consented duration or frequency...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports denying data access based on frequency limits through its throttling mechanisms. The system can enforce li...

</details>

---

</details>

<details>
<summary><strong>Error Handling</strong> — 10 gap(s) | 5 not supported | 5 partial</summary>

### Error Handling

*10 gap(s) identified*

#### GAP_0018: ATOM_039

**Requirement:** HTTP response code 201 Created MUST be returned for successful POST requests where Payment Initiation or Consent Request was correctly performed

- **Strength:** `MUST`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Yes, this repository supports returning an HTTP `201 Created` response code for successful POST requests related to certain creation operations, including ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports returning an HTTP 201 Created status code for successful POST requests related to various resource creatio...

</details>

---

#### GAP_0038: ATOM_230

**Requirement:** TPP message category SHALL only permit "ERROR" or "WARNING" values

- **Strength:** `SHALL`
- **Section:** `14.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Based on the provided codebase context, there is no direct support or explicit configuration for a "TPP message category" that is restricted to "ERROR" or ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports logging with various categories, including "ERROR" and "WARN"    . However, the documentation indicates th...

</details>

---

#### GAP_0055: ATOM_046

**Requirement:** When an OAuth2 token is invalid, the system shall return an HTTP 401 Unauthorized response with Content-Type application/problem+json

- **Strength:** `SHALL`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports returning an HTTP 401 Unauthorized response when an OAuth2 token is invalid. However, the provided context doe...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support returning an HTTP 401 Unauthorized response when an OAuth2 token is invalid. However, the `Conte...

</details>

---

#### GAP_0091: ATOM_048

**Requirement:** Error responses shall include a human-readable title describing the error condition

- **Strength:** `SHALL`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports error responses that include a human-readable title (referred to as "message" in the codebase) describing the ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Yes, this repository supports error responses that include a human-readable title describing the error condition.    \n\n## Implementation Details\n\nThe...

</details>

---

#### GAP_0109: ATOM_047

**Requirement:** Error responses shall include a type field with URI reference to the specific error code documentation

- **Strength:** `SHALL`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support error responses that include a `type` field, but it does not explicitly use a URI reference to speci...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, defines error responses in its OpenAPI/Swagger specifications that include a `moreInfo` field intended to contain a...

</details>

---

#### GAP_0150: ATOM_044

**Requirement:** The Content-Type header MUST be set to application/json when using NextGenPSD2 specific error information

- **Strength:** `MANDATORY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, contains integration tests that demonstrate how `Content-Type: application/json` is used in various API interactions, p...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support setting the `Content-Type` header to `application/json` for error responses, particularly within...

</details>

---

#### GAP_0152: ATOM_045

**Requirement:** The Content-Type header MUST be set to application/problem+json when using standardised RFC7807 error information

- **Strength:** `MANDATORY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not explicitly support setting the `Content-Type` header to `application/problem+json` for RFC7807 error informati...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, the repository does not explicitly support setting the `Content-Type` header to `application/problem+json` for RFC78...

</details>

---

#### GAP_0157: ATOM_049

**Requirement:** Error responses may include additional error details limited to 500 characters

- **Strength:** `MAY`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': "This repository, `wso2/product-is`, includes mechanisms for validating error responses, but it does not explicitly enforce a 500-character limit on the `de...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository defines an `Error` object in its OpenAPI specifications that includes a `description` field for detailed error messages. While the schema...

</details>

---

#### GAP_0164: ATOM_051

**Requirement:** Error responses may include an additionalErrors array for multiple related errors

- **Strength:** `MAY`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not explicitly support an `additionalErrors` array for multiple related errors in its API responses based on the p...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Yes, this repository supports error responses that may include an `additionalErrors` array for multiple related errors.    This is defined within the Ope...

</details>

---

#### GAP_0171: ATOM_043

**Requirement:** Additional error information with messageCode field SHALL be mandatory when using NextGenPSD2 specific error solution

- **Strength:** `MANDATORY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the inclusion of error information, including a `messageCode` field, within API error responses. The...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support error responses with a `code` and `message` field, but there is no explicit mention or implement...

</details>

---

</details>

<details>
<summary><strong>Event Notification</strong> — 1 gap(s) | 1 partial</summary>

### Event Notification

*1 gap(s) identified*

#### GAP_0158: ATOM_090

**Requirement:** ASPSP should inform TPP to notify PSU about decoupled authentication requirement via PSU Message

- **Strength:** `SHOULD`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. #Real Time Event Notification

Real Time Event Notification is a method where banks will immediately notify the TPP about any events that occur, without waiting for a request from the TPP. This functi...

2. ### Data 
The following table explains the data available in `NotificationCreationDTO`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| cli...

3. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, WSO2 Identity Server, appears to have capabilities related to sending notifications, but there is no direct evidence within the provided s...

</details>

---

</details>

<details>
<summary><strong>Funds Confirmation</strong> — 5 gap(s) | 4 not supported | 1 partial</summary>

### Funds Confirmation

*5 gap(s) identified*

#### GAP_0057: ATOM_113

**Requirement:** The fundsAvailable field SHALL be included when ASPSP supports funds check, funds check has been performed, and transactionStatus is ACTC, ACWC or ACCP

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support the `fundsAvailable` field or the specific conditions related to ASPSP funds checks...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, this repository, WSO2 API Manager, does not appear to directly support the `fundsAvailable` field or the specific co...

</details>

---

#### GAP_0083: ATOM_208

**Requirement:** ASPSP SHALL return HTTP response code 200 for successful confirmation of funds requests.

- **Strength:** `SHALL`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to be an Identity Server and does not directly support the role of an Account Servicing Payment Service Provide...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support returning an HTTP response code 200 for successful requests, including those that might be relat...

</details>

---

#### GAP_0084: ATOM_209

**Requirement:** ASPSP MUST return fundsAvailable as true if sufficient funds are available at the time of the request, false otherwise.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': "This repository, `wso2/product-is`, does not appear to directly support the specific requirement of an ASPSP (Account Servicing Payment Service Provider) r...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, specifically within the `wso2/product-apim` project, contains a sample JAX-RS service that demonstrates a payment processing flow, inclu...

</details>

---

#### GAP_0102: ATOM_063

**Requirement:** The system shall provide optional fundsAvailable boolean data element with transaction status codes ACTC, ACWC, and ACCP to indicate funds check results

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Based on the provided code snippets, this repository does not appear to support the `fundsAvailable` boolean data element with transaction status codes ACT...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, the repository `wso2/product-apim` does not appear to directly support an optional `fundsAvailable` boolean data ele...

</details>

---

#### GAP_0166: ATOM_037

**Requirement:** The POST funds-confirmations endpoint SHALL be mandatory for checking whether a specific amount is available at point of time of the request on an account

- **Strength:** `MANDATORY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Based on the provided codebase context, there is no direct support for a `POST /funds-confirmations` endpoint for checking fund availability on an account ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, the repository `wso2/product-apim` does not appear to directly support a `POST /funds-confirmations` endpoint for ch...

</details>

---

</details>

<details>
<summary><strong>General</strong> — 11 gap(s) | 4 not supported | 7 partial</summary>

### General

*11 gap(s) identified*

#### GAP_0039: ATOM_199

**Requirement:** The _links field SHALL be mandatory and contain hyperlinks for the transaction flow including scaStatus link.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the inclusion of a `_links` field containing hyperlinks within API responses, particularly for pagin...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to have mechanisms for handling and processing various types of links, but there is no direct evidence with...

</details>

---

#### GAP_0048: ATOM_109

**Requirement:** The X-Request-ID header SHALL be mandatory and contain a UUID unique to the call as determined by the initiating party

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to explicitly enforce the `X-Request-ID` header as mandatory with a UUID format for all API calls. Whil...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not explicitly support a mandatory `X-Request-ID` header that contains a UUID and causes a request to fail if ...

</details>

---

#### GAP_0051: ATOM_010

**Requirement:** ASPSPs must accept at least the specified basic character set including letters, numbers, and common punctuation

- **Strength:** `MUST`
- **Section:** `eef9ab97432c - 4.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports character set validation for usernames, which is relevant to the requirement that ASPSPs must accept a specifi...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, demonstrates some support for handling special characters in various contexts, including API resource names, endpoi...

</details>

---

#### GAP_0066: ATOM_118

**Requirement:** The X-Request-ID header SHALL be mandatory and contain a UUID that is unique to the call

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to explicitly enforce the `X-Request-ID` header as mandatory with a UUID format for all API calls. Howe...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not explicitly support a mandatory `X-Request-ID` header containing a UUID that is unique to the call, nor doe...

</details>

---

#### GAP_0067: ATOM_173

**Requirement:** The X-Request-ID header MUST be included as a UUID that uniquely identifies the request as determined by the initiating party.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to explicitly support the `X-Request-ID` header as a UUID that uniquely identifies the request as deter...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports the inclusion of a unique message ID, which is a UUID, in messages. While it doesn\'t explicitly refer to ...

</details>

---

#### GAP_0094: ATOM_179

**Requirement:** The response MUST echo back the X-Request-ID header value from the request.

- **Strength:** `MUST`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Based on the provided code snippets, this repository, `wso2/product-is`, does not appear to explicitly support echoing back the `X-Request-ID` header value...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided codebase, there is no direct support for echoing back the `X-Request-ID` header value from the request. The relevant configuration ...

</details>

---

#### GAP_0130: ATOM_072

**Requirement:** The system shall provide hyperlinks with semantic tags in the _links data element to guide TPP through API processes for payment initiation and account information services

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the inclusion of hyperlinks with semantic tags in API responses, specifically within a `_links` data element, ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to be an API Management solution. The provided code snippets do not directly show support for the `_links` ...

</details>

---

#### GAP_0133: ATOM_187

**Requirement:** The X-Request-ID header field SHALL be mandatory and contain a UUID that is unique to the call as determined by the initiating party.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not explicitly enforce the `X-Request-ID` header field to be mandatory or to contain a UUID in all requests as a c...

2. [wso2/product-apim]
[{'type': 'text', 'text': "This repository, `wso2/product-apim`, does not explicitly support a mandatory `X-Request-ID` header field containing a UUID for all requests. However, it...

</details>

---

#### GAP_0148: ATOM_075

**Requirement:** The system may include additional hyperlinks beyond those specified in related API calls and shall document these in ASPSP PSD2 documentation

- **Strength:** `MAY`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, WSO2 Identity Server, includes documentation and configuration for various API endpoints that may contain hyperlinks. The system\'s API la...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, WSO2 API Manager, supports documenting additional hyperlinks within its API documentation. This is primarily managed through the API Pub...

</details>

---

#### GAP_0167: ATOM_076

**Requirement:** The system may add additional data attributes to response messages and shall document these extensions in ASPSP XS2A interface documentation

- **Strength:** `MAY`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the addition of data attributes to response messages through its API layer, particularly within the context of...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports adding additional data attributes to response messages through its XPath Extension Framework and provides ...

</details>

---

#### GAP_0174: ATOM_074

**Requirement:** The system should use relative links in hyperlink steering to save space

- **Strength:** `SHOULD`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': "This repository, `wso2/product-is`, supports the use of relative links in API responses, particularly for pagination links. The API Layer is designed to pr...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support the use of relative links in API responses, particularly for `Location` headers and pagination l...

</details>

---

</details>

<details>
<summary><strong>Payment Initiation</strong> — 24 gap(s) | 12 not supported | 12 partial</summary>

### Payment Initiation

*24 gap(s) identified*

#### GAP_0002: ATOM_115

**Requirement:** When XML status format is chosen, the system SHALL follow XML schema definitions of the original pain.001 schema

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. <?xml version="1.0" encoding="UTF-8"?>
<!--
 ~ Copyright (c) 2024, WSO2 LLC. (https://www.wso2.com).
 ~
 ~ WSO2 LLC. licenses this file to you under the Apache License,
 ~ Version 2.0 (the "License");...

2. x-fapi-interaction-id:
      in: "header"
      name: "x-fapi-interaction-id"
      required: false
      description: "An RFC4122 UID used as a correlation id."
      schema:
        type: "string"

...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0005: ATOM_056

**Requirement:** The system shall support transaction status ACWC (AcceptedWithChanges) to indicate successful checks with ASPSP-applied changes to payment initiation such as requested execution date modifications

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

2. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0011: ATOM_023

**Requirement:** Payment cancellation SHALL be divided into two steps: DELETE the corresponding resource, and start an authorisation process for the cancellation by the PSU where needed.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'The WSO2 Financial Services Accelerator supports payment cancellation through a two-step process involving a `DELETE` request on the pa...

</details>

---

#### GAP_0017: ATOM_104

**Requirement:** ASPSPs MUST return transaction status ACTC for multilevel SCA when first authorization is completed

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

3. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0026: ATOM_066

**Requirement:** The system shall set transaction status to CANC (Cancelled) after successful payment cancellation and maintain this status while the resource remains addressable

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, the WSO2 Financial Services Accelerator, supports setting a transaction status to `CANC` (Cancelled) after a successfu...

</details>

---

#### GAP_0029: ATOM_054

**Requirement:** Final payment transaction status shall be either RJCT (Rejected) or ACSC (AcceptedSettlementCompleted) at the end of the payment process

- **Strength:** `SHALL`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

2. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0030: ATOM_106

**Requirement:** The system SHALL support GET request to retrieve transaction status at endpoint /v1/{payment-service}/{payment-product}/{paymentId}/status

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

2. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

3. ## Publish Open Banking APIs

!!! note
    WSO2 Open Banking Accelerator supports Accounts flow, Payments flow and Confirmation of Funds flow. Publish all three APIs before trying out the flows.

1. S...

</details>

---

#### GAP_0031: ATOM_057

**Requirement:** The system shall support transaction status ACCP (AcceptedCustomerProfile) to indicate positive financial risk profile and PSU funds availability checks

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0033: ATOM_062

**Requirement:** The system shall support transaction status PART (PartiallyAccepted) for bulk payments when not all payments are processed successfully despite completed authorizations

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

2. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0040: ATOM_058

**Requirement:** The system shall support transaction status ACFC (AcceptedFundsChecked) to indicate positive customer profile and funds availability verification

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

2. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

3. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

</details>

---

#### GAP_0043: ATOM_231

**Requirement:** Amount values SHALL be represented with fractional digits compliant to currency definition, up to 14 significant figures, with dot as decimal separator

- **Strength:** `SHALL`
- **Section:** `14.3`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, specifically within the WSO2 Financial Services Accelerator, supports amount values with fractional digits and a dot a...

</details>

---

#### GAP_0054: ATOM_086

**Requirement:** ASPSP must provide confirmation code as query parameter when requesting transaction authorization confirmation

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

3. obWritePaymentConsentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
      ...

</details>

---

#### GAP_0068: ATOM_117

**Requirement:** The payment-service path parameter SHALL accept only the values 'payments', 'bulk-payments', and 'periodic-payments'

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

3. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

</details>

---

#### GAP_0076: ATOM_087

**Requirement:** TPP must validate confirmationCode semantics in transaction authorization confirmation response

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. The **API Consumer Validation** service in WSO2 Open Banking allows banks to validate API consumers from the National 
Competent Authorities (NCAs). This is done by validating the transport layer cert...

2. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

3. x-fapi-interaction-id:
      in: "header"
      name: "x-fapi-interaction-id"
      required: false
      description: "An RFC4122 UID used as a correlation id."
      schema:
        type: "string"

...

</details>

---

#### GAP_0095: ATOM_022

**Requirement:** The specification SHALL support cancellation of payment initiations by PISPs starting from version 1.2.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. The **API Consumer Validation** service in WSO2 Open Banking allows banks to validate API consumers from the National 
Competent Authorities (NCAs). This is done by validating the transport layer cert...

3. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0097: ATOM_122

**Requirement:** The payment cancellation DELETE request SHALL return HTTP 202 if authorisation of the cancellation by the PSU is needed

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

3. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

</details>

---

#### GAP_0101: ATOM_124

**Requirement:** The ASPSP SHALL check if the payment-product matches the payment initiation addressed by paymentId

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

2. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0105: ATOM_105

**Requirement:** ASPSPs MUST return transaction status PATC for multilevel SCA when payment is partially authorized

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

3. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0112: ATOM_108

**Requirement:** The ASPSP SHALL validate that the payment-product matches the payment initiation addressed by paymentId

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

2. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0117: ATOM_107

**Requirement:** The payment-service path parameter SHALL accept values 'payments', 'bulk-payments', and 'periodic-payments'

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

3. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

</details>

---

#### GAP_0132: ATOM_055

**Requirement:** The system shall support transaction status ACTC (AcceptedTechnicalCorrect) to indicate successful PSU authentication and syntactical/semantical product checks for batch booking processes

- **Strength:** `SHALL`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

2. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

3. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

</details>

---

#### GAP_0142: ATOM_125

**Requirement:** The transactionStatus field SHALL be mandatory in payment cancellation response body when HTTP code 202 is returned

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

2. x-fapi-interaction-id:
      in: "header"
      name: "x-fapi-interaction-id"
      required: false
      description: "An RFC4122 UID used as a correlation id."
      schema:
        type: "string"

...

3. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

</details>

---

#### GAP_0163: ATOM_114

**Requirement:** For XML encoded Payment Initiation Requests, the ASPSP MAY return status as pain.002 structure or JSON structure

- **Strength:** `MAY`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

2. obWritePayment2:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

3. obWriteConsent4:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
        - "Risk"
      properties:
        Data:
          type: "object"
          additionalP...

</details>

---

#### GAP_0169: ATOM_081

**Requirement:** The TPP MAY send an SCA status request to follow the SCA process during implicit authorisation

- **Strength:** `MAY`
- **Section:** `648825991d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

2. The **API Consumer Validation** service in WSO2 Open Banking allows banks to validate API consumers from the National 
Competent Authorities (NCAs). This is done by validating the transport layer cert...

3. x-fapi-interaction-id:
      in: "header"
      name: "x-fapi-interaction-id"
      required: false
      description: "An RFC4122 UID used as a correlation id."
      schema:
        type: "string"

...

</details>

---

</details>

<details>
<summary><strong>Security</strong> — 20 gap(s) | 6 not supported | 14 partial</summary>

### Security

*20 gap(s) identified*

#### GAP_0015: ATOM_194

**Requirement:** The PSU-IP-Address header SHALL be contained if and only if the request was actively initiated by the PSU.

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, WSO2 Identity Server, does not appear to have explicit support for handling a `PSU-IP-Address` header with the specific condition "if and ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided codebase snippets, there is no direct evidence or implementation details regarding a "PSU-IP-Address" header or its conditional inc...

</details>

---

#### GAP_0021: ATOM_226

**Requirement:** PKCE code_challenge parameter SHALL be included in authorization request according to RFC 7636 to prevent code injection attacks

- **Strength:** `SHALL`
- **Section:** `13.1`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

2. ### Authorization Request

WSO2 Open Banking Accelerator supports the following security features and fulfil FAPI requirements 
during Authorization flows:

  - OIDC Hybrid Flow
    - Request object v...

3. ### Validate method

This method lets you perform validations at the filter level. Given below is the method signature.

``` java
void validate(ServletRequest request, String clientId) throws TokenFil...

</details>

---

#### GAP_0069: ATOM_205

**Requirement:** ASPSP MUST include Digest header field if and only if the Signature element is contained in the request header.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

2. ### Validate method

This method lets you perform validations at the filter level. Given below is the method signature.

``` java
void validate(ServletRequest request, String clientId) throws TokenFil...

3. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the inclusion of a Digest header field in SAML requests, which is related to the presence of a Signa...

</details>

---

#### GAP_0073: ATOM_085

**Requirement:** TPP must control session fixation using the state parameter during redirect SCA approach

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. #Using Sample Resources

Following configs can be used in test-config.xml to use sample SSA and keystores for DCR tests.

    <DCR>
        <SSAPath>Path.To.Directory/ssa.txt</SSAPath>
        <!-- SS...

2. ### Run tests

1. Use a tool and convert the private key (tpp.com.key) to a JWK. Use this JWK to update the value of the **keys** 
   array element in the JSON configuration.
2. Log in to the test sui...

3. #Details for Tsteing Purposes

SSA SoftwareId - oQ4KoaavpOuoE7rvQsZEOV
SSA Redirect Uri - https://www.google.com/redirects/redirect1


Sample Keystore information:
- Signing Kid = sCekNgSWIauQ34klRhDG...

</details>

---

#### GAP_0074: ATOM_029

**Requirement:** TPPs SHALL keep the TPP-Redirect-URI used within all authorisation processes for a specific transaction constant during the lifecycle of that transaction.

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

2. # redirect_endpoint config defines the user's succesfull authorisations redirect endpoint. This page displays the succesful CIBA flow completions.
redirect_endpoint = "https://localhost:9446/authentic...

3. ### Resource Request

After an API consumer application obtains an access token, it is used to invoke a resource endpoint. In this request, 
the following validations will be performed:

- Token valid...

</details>

---

#### GAP_0085: ATOM_001

**Requirement:** TLS connections must use TLS version 1.2 or higher for communication between TPP and ASPSP

- **Strength:** `MUST`
- **Section:** `eef9ab97432c - 4.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

2. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

3. ## DefaultTokenFilter 

Customize the following class to modify the token request, response, or error handling. 
``` java
com.wso2.openbanking.accelerator.identity.token.DefaultTokenFilter
```

!!! no...

</details>

---

#### GAP_0089: ATOM_210

**Requirement:** When a TPP includes a digital signature, the TPP must include a Digest header containing a hash of the message body using SHA-256 or SHA-512 algorithms

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. Certificate (QWAC) and Qualified Certificates for Electronic Seals (QSealC) to secure the transport layer and application layer with the API consumer. ####Qualified Web Authentication Certificate (QWA...

2. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

3. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the use of SHA-256 and SHA-512 algorithms for hashing in various contexts, including DPoP (Demonstrating Proof...

</details>

---

#### GAP_0100: ATOM_211

**Requirement:** For messages without a body, the Digest header must contain the hash of an empty byte list

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

1. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

2. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support the automatic generation of a `Digest` header containing the hash of an empty byte ...

3. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to have some support for Digest Authentication, but it does not explicitly confirm or implement the specifi...

</details>

---

#### GAP_0113: ATOM_214

**Requirement:** The algorithm parameter in the Signature header is mandatory and must identify the same signature algorithm as the TPP's public key in the certificate

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

2. ## DefaultTokenFilter 

Customize the following class to modify the token request, response, or error handling. 
``` java
com.wso2.openbanking.accelerator.identity.token.DefaultTokenFilter
```

!!! no...

3. #Details for Tsteing Purposes

SSA SoftwareId - oQ4KoaavpOuoE7rvQsZEOV
SSA Redirect Uri - https://www.google.com/redirects/redirect1


Sample Keystore information:
- Signing Kid = sCekNgSWIauQ34klRhDG...

</details>

---

#### GAP_0114: ATOM_215

**Requirement:** The headers parameter in the Signature header must include digest and x-request-id

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

2. ## DefaultTokenFilter 

Customize the following class to modify the token request, response, or error handling. 
``` java
com.wso2.openbanking.accelerator.identity.token.DefaultTokenFilter
```

!!! no...

3. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

</details>

---

#### GAP_0123: ATOM_216

**Requirement:** The headers parameter must conditionally include psu-id if and only if PSU-ID header is present in the HTTP request

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

1. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

2. [wso2/product-is]
[{'type': 'text', 'text': "This repository, `wso2/product-is`, appears to support the conditional inclusion of a `psu-id` parameter in headers, specifically within the context of DPo...

3. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support conditional header manipulation, which could be used to implement the requirement of conditional...

</details>

---

#### GAP_0127: ATOM_217

**Requirement:** The headers parameter must conditionally include psu-corporate-id if and only if PSU-Corporate-ID header is present in the HTTP request

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

2. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

3. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support the conditional inclusion of a `psu-corporate-id` header based on the presence of a...

</details>

---

#### GAP_0131: ATOM_218

**Requirement:** The headers parameter must conditionally include tpp-redirect-uri if and only if TPP-Redirect-URI header is present in the HTTP request

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

2. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

3. # redirect_endpoint config defines the user's succesfull authorisations redirect endpoint. This page displays the succesful CIBA flow completions.
redirect_endpoint = "https://localhost:9446/authentic...

</details>

---

#### GAP_0149: ATOM_025

**Requirement:** It is strongly RECOMMENDED to send PSU context data elements in all request messages within payment initiation or consent initiation transaction flows with PSU authentication involved.

- **Strength:** `RECOMMENDED`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Multi auth user flows

For example of multi authorisation flow, we can think joint account scenario where all the users need to approve the consent. Below steps are mainly involved for multi auth u...

2. ## Assumptions
- User's mobile number should be configured.
- Users will receive the notification as web links to authenticate and authorize the consent.
- For multiple users involved scenarios, Ident...

3. ### Sending CIBA Request

1. Invoke the CIBA request available in the [Postman collection](https://www.getpostman.com/collections/34a4fa4b9184ae3b4821).

       - `login_hint` parameter inside the req...

</details>

---

#### GAP_0151: ATOM_091

**Requirement:** TPP should follow OAuth Security Best Practice definitions as defined in OA-SecTop reference

- **Strength:** `RECOMMENDED`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

2. ### Authorization Request

WSO2 Open Banking Accelerator supports the following security features and fulfil FAPI requirements 
during Authorization flows:

  - OIDC Hybrid Flow
    - Request object v...

3. # API Security Open Banking allows API consumers to access financial data through open APIs, which requires greater API security. Therefore, open banking standards provide guidelines for security impl...

</details>

---

#### GAP_0153: ATOM_028

**Requirement:** URIs provided by TPPs in TPP-Redirect-URI or TPP-Nok-Redirect-URI SHOULD comply with the domain secured by the eIDAS QWAC certificate of the TPP in the field CN or SubjectAltName.

- **Strength:** `SHOULD`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. Certificate (QWAC) and Qualified Certificates for Electronic Seals (QSealC) to secure the transport layer and application layer with the API consumer. ####Qualified Web Authentication Certificate (QWA...

2. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

3. #Details for Tsteing Purposes

SSA SoftwareId - oQ4KoaavpOuoE7rvQsZEOV
SSA Redirect Uri - https://www.google.com/redirects/redirect1


Sample Keystore information:
- Signing Kid = sCekNgSWIauQ34klRhDG...

</details>

---

#### GAP_0154: ATOM_033

**Requirement:** ASPSPs MAY tokenise card-account-id parameters such that actual card account or card numbers like IBANs or PANs are not part of the path definitions for data protection reasons

- **Strength:** `MAY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ## Assumptions
- User's mobile number should be configured.
- Users will receive the notification as web links to authenticate and authorize the consent.
- For multiple users involved scenarios, Ident...

2. ### Configuring a custom validator

1. Once you implement the custom validator, build a JAR file for the project and place it in the 
`<IS_HOME>/repository/components/dropins` directory.

2. Open the ...

3. # API Security Open Banking allows API consumers to access financial data through open APIs, which requires greater API security. Therefore, open banking standards provide guidelines for security impl...

</details>

---

#### GAP_0155: ATOM_005

**Requirement:** ASPSP may require TPP to sign request messages at application layer

- **Strength:** `MAY`
- **Section:** `eef9ab97432c - 4.2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

2. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

3. ## Assumptions
- User's mobile number should be configured.
- Users will receive the notification as web links to authenticate and authorize the consent.
- For multiple users involved scenarios, Ident...

</details>

---

#### GAP_0156: ATOM_030

**Requirement:** All methods submitted by a TPP that address dynamically created resources in this API MAY only apply to resources which have been created by the same TPP before.

- **Strength:** `MAY`
- **Section:** `508687390798`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Resource Request

After an API consumer application obtains an access token, it is used to invoke a resource endpoint. In this request, 
the following validations will be performed:

- Token valid...

2. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

3. ### How to use mediation artifacts 

1. Once the maven build is successful, navigate to the **fs-apim-mediation-artifacts/target** folder to get the zip file containing all the mediation policies,cust...

</details>

---

#### GAP_0159: ATOM_174

**Requirement:** The PSU-IP-Address header SHOULD be included when the request was actively initiated by the PSU, containing the forwarded IP address between PSU and TPP.

- **Strength:** `SHOULD`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\c11d1a51-22fa-4934-a589-afb65d38f081\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

1. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

2. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the forwarding of client IP addresses through the use of a `RemoteIpValve` in its Tomcat configurati...

3. [wso2/product-apim]
[{'type': 'text', 'text': "This repository does not appear to directly support the automatic inclusion of a `PSU-IP-Address` header containing the forwarded IP address when a reque...

</details>

---

</details>

## Critical Gaps Requiring Immediate Attention

The following requirements are **not supported** by the current WSO2 implementation:

| Gap ID | Requirement | Capability | Strength |
|--------|-------------|------------|----------|
| GAP_0003 | ASPSP SHALL provide TPPs with configuration data c... | Authentication | SHALL |
| GAP_0005 | The system shall support transaction status ACWC (... | Payment Initiation | SHALL |
| GAP_0013 | ASPSPs MUST return ASPSP-SCA-Approach header with ... | Authentication | MUST |
| GAP_0015 | The PSU-IP-Address header SHALL be contained if an... | Security | SHALL |
| GAP_0016 | The POST /v1/{payment-service}/{payment-product}/{... | Authentication | SHALL |
| GAP_0017 | ASPSPs MUST return transaction status ACTC for mul... | Payment Initiation | MUST |
| GAP_0027 | The ASPSP shall support Global Consent model where... | Consent Management | SHALL |
| GAP_0028 | The scaStatus field SHALL be mandatory in the auth... | Authentication | SHALL |
| GAP_0033 | The system shall support transaction status PART (... | Payment Initiation | SHALL |
| GAP_0034 | The TPP-Redirect-URI header SHALL be mandatory for... | Authentication | SHALL |
| GAP_0037 | ASPSPs MUST validate eIDAS certificate request syn... | Certificate Management | MUST |
| GAP_0038 | TPP message category SHALL only permit "ERROR" or ... | Error Handling | SHALL |
| GAP_0040 | The system shall support transaction status ACFC (... | Payment Initiation | SHALL |
| GAP_0045 | Standing order information requests MUST use booki... | Account Information | MUST |
| GAP_0048 | The X-Request-ID header SHALL be mandatory and con... | General | SHALL |
| GAP_0050 | TPP MUST generate a nonce for the challenge parame... | Authentication | MUST |
| GAP_0052 | The API MUST support a GET endpoint at /v1/account... | Account Information | MUST |
| GAP_0053 | The API SHALL support multiple level SCA where a t... | Authentication | SHALL |
| GAP_0054 | ASPSP must provide confirmation code as query para... | Payment Initiation | MUST |
| GAP_0056 | The system shall provide SCA process status inform... | Authentication | SHALL |
| GAP_0057 | The fundsAvailable field SHALL be included when AS... | Funds Confirmation | SHALL |
| GAP_0061 | The system shall set transaction status to PATC (P... | Authentication | SHALL |
| GAP_0065 | ASPSPs SHALL enable direct start of Redirect SCA p... | Authentication | SHALL |
| GAP_0066 | The X-Request-ID header SHALL be mandatory and con... | General | SHALL |
| GAP_0067 | The X-Request-ID header MUST be included as a UUID... | General | MUST |
| GAP_0068 | The payment-service path parameter SHALL accept on... | Payment Initiation | SHALL |
| GAP_0069 | ASPSP MUST include Digest header field if and only... | Security | MUST |
| GAP_0076 | TPP must validate confirmationCode semantics in tr... | Payment Initiation | MUST |
| GAP_0080 | When the underlying account is a multicurrency acc... | Account Information | SHALL |
| GAP_0081 | The signing basket SHALL get the status of being f... | Authentication | SHALL |
| GAP_0082 | The API SHALL support signing of a group of transa... | Authentication | SHALL |
| GAP_0084 | ASPSP MUST return fundsAvailable as true if suffic... | Funds Confirmation | MUST |
| GAP_0089 | When a TPP includes a digital signature, the TPP m... | Security | MUST |
| GAP_0093 | The system SHALL support multicurrency accounts by... | Account Information | SHALL |
| GAP_0095 | The specification SHALL support cancellation of pa... | Payment Initiation | SHALL |
| GAP_0100 | For messages without a body, the Digest header mus... | Security | MUST |
| GAP_0102 | The system shall provide optional fundsAvailable b... | Funds Confirmation | SHALL |
| GAP_0104 | TPP certificate must be compliant with EBA-RTS req... | Certificate Management | MUST |
| GAP_0105 | ASPSPs MUST return transaction status PATC for mul... | Payment Initiation | MUST |
| GAP_0109 | Error responses shall include a type field with UR... | Error Handling | SHALL |
| GAP_0114 | The headers parameter in the Signature header must... | Security | MUST |
| GAP_0117 | The payment-service path parameter SHALL accept va... | Payment Initiation | SHALL |
| GAP_0118 | The system shall support consent status 'terminate... | Consent Management | SHALL |
| GAP_0119 | The TPP-Redirect-URI header SHALL be mandatory for... | Authentication | SHALL |
| GAP_0121 | The GET /v1/card-accounts/{account-id}/balances en... | Account Information | SHALL |
| GAP_0122 | Electronic signature of TPP must be based on a qua... | Certificate Management | MUST |
| GAP_0124 | The system SHALL include PSU-IP-Address header whe... | Data Access | SHALL |
| GAP_0125 | The API SHALL support signing of a group of transa... | Authentication | SHALL |
| GAP_0129 | Payment resources that need to be signed n times S... | Authentication | SHALL |
| GAP_0132 | The system shall support transaction status ACTC (... | Payment Initiation | SHALL |
| GAP_0133 | The X-Request-ID header field SHALL be mandatory a... | General | SHALL |
| GAP_0134 | The GET /v1/accounts/{account-id}/transactions end... | Account Information | SHALL |
| GAP_0142 | The transactionStatus field SHALL be mandatory in ... | Payment Initiation | SHALL |
| GAP_0147 | The ASPSP MAY support deltaList parameter to indic... | Account Information | MAY |
| GAP_0152 | The Content-Type header MUST be set to application... | Error Handling | MANDATORY |
| GAP_0153 | URIs provided by TPPs in TPP-Redirect-URI or TPP-N... | Security | SHOULD |
| GAP_0157 | Error responses may include additional error detai... | Error Handling | MAY |
| GAP_0166 | The POST funds-confirmations endpoint SHALL be man... | Funds Confirmation | MANDATORY |
| GAP_0170 | ASPSPs MAY offer the signing-baskets endpoint to s... | Authentication | MAY |
| GAP_0171 | Additional error information with messageCode fiel... | Error Handling | MANDATORY |
| GAP_0173 | When offering the signing basket function, ASPSPs ... | Authentication | MAY |

## Recommendations

### High Priority
- Address **61** unsupported requirements through custom development or third-party solutions

### Medium Priority
- Review **112** partially supported requirements for configuration or extension opportunities

---

*Generated by Open Banking Compliance Agentic Workflow*
*Analysis powered by WSO2 Knowledge Base (231 requirements analyzed)*