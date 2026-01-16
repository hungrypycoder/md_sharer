# Open Banking Compliance Analysis Report

**Report ID:** `0c89493c-8601-4ae1-ad90-6602c7cd089e`  
**Generated:** January 16, 2026 at 03:19 UTC  
**Specification:** 838576b0-1da9-498e-bcd3-b1f1d46287fc

---

## Executive Summary

| Metric | Value |
|--------|-------|
| Total Requirements Analyzed | **217** |
| Requirements with Gaps | **162** (74.7%) |
| Compliance Rate | **0.0%** |

### Support Level Breakdown

| Status | Count | Percentage |
|--------|-------|------------|
| Fully Supported | 0 | 0.0% |
| Partially Supported | 101 | 46.5% |
| Not Supported | 56 | 25.8% |
| Requires Configuration | 0 | 0.0% |
| Unknown | 5 | 2.3% |

### Dependency Analysis

| Property | Value |
|----------|-------|
| Total Dependencies | 0 |
| Graph Type | Valid DAG |
| Max Dependency Depth | 0 |
| Root Requirements | 217 |
| Leaf Requirements | 217 |

---

## Gap Analysis by Capability

<details>
<summary><strong>Account Information</strong> — 16 gap(s) | 6 not supported | 10 partial</summary>

### Account Information

*16 gap(s) identified*

#### GAP_0003: ATOM_163

**Requirement:** The system SHALL support reading card account balance data from a given card account addressed by account-id via GET /v1/card-accounts/{account-id}/balances endpoint

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

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

#### GAP_0015: ATOM_148

**Requirement:** Standing order details MUST include frequency and execution rule information

- **Strength:** `MUST`
- **Section:** `f30dd2c91d5e`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'Yes, the WSO2 Financial Services Accelerator repository supports standing order details including frequency and execution rule informat...

</details>

---

#### GAP_0038: ATOM_170

**Requirement:** The system SHALL support reading card account transaction data via GET /v1/card-accounts/{account-id}/transactions endpoint

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. This document provides step by step instructions to tryout the flow with Manual Client Registration. This includes

- Setting up WSO2 FInancial Services Key Manager
- Create application using Manual C...

</details>

---

#### GAP_0040: ATOM_171

**Requirement:** The system SHALL support bookingStatus query parameter with mandatory values 'booked', 'pending', and 'both'

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (1 sources)</summary>

1. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'The WSO2 Financial Services Accelerator supports the `bookingStatus` query parameter with mandatory values \'Booked\' and \'Pending\' f...

</details>

---

#### GAP_0041: ATOM_146

**Requirement:** The system MUST distinguish between booked and pending transactions

- **Strength:** `MUST`
- **Section:** `f30dd2c91d5e`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

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

2. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, `wso2/financial-services-accelerator`, supports distinguishing between booked and pending transactions through its API...

</details>

---

#### GAP_0045: ATOM_140

**Requirement:** The system SHALL support bookingStatus values of 'booked', 'pending', 'both', and 'information' with booked being mandatory

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0048: ATOM_172

**Requirement:** The system SHALL support dateFrom query parameter as conditional requirement when no delta access is required

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

1. If this is not populated, the permissions will be open ended.All
              dates in the JSON payloads are represented in ISO 8601 date-time
              format.

              All date-time field...

2. All date-time fields in responses must include the timezone. An example is
      below:

      2017-04-05T10:43:07+00:00
    type: string
    format: date-time
  StatusUpdateDateTime:
    description:...

3. For transaction entries subject to availability/float and for which
      availability information is provided, the value date must not be used. In
      this case the availability component identifie...

</details>

---

#### GAP_0049: ATOM_132

**Requirement:** Account access endpoints SHALL separate usual bank accounts and credit card accounts since data is usually separated in ASPSP backend

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

2. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

3. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'The WSO2 Financial Services Accelerator supports the separation of bank accounts and credit card accounts through its API definitions a...

</details>

---

#### GAP_0051: ATOM_147

**Requirement:** Account transaction requests MUST support bookingStatus query parameter

- **Strength:** `MUST`
- **Section:** `f30dd2c91d5e`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ### Consent Initiation
- In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. A sample consent initiation requ...

2. ### Authorize a consent

The bank sends the request to the customer stating the accounts and information that the API consumer wishes to access.
    
       
  1. Generate the request object by signin...

3. swagger: '2.0'
info:
  title: AccountandTransactionAPI
  description: Swagger for Account and Transaction API Specification
  version: v3.1
basePath: /open-banking/{version}/aisp
tags:
  - name: Accou...

</details>

---

#### GAP_0058: ATOM_134

**Requirement:** The system SHALL support multi-currency accounts by setting currency code to 'XXX' for aggregated account views

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. Usage: If not present, credit line is not included in
                          the balance amount of the account.
                        type: boolean
                      Type:
                   ...

</details>

---

#### GAP_0066: ATOM_136

**Requirement:** The system SHALL accept an optional withBalance query parameter to include booking balance in account details response

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
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

#### GAP_0082: ATOM_139

**Requirement:** The system SHALL support transaction list retrieval with dateFrom, dateTo, and bookingStatus query parameters

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. If this is not populated, the permissions will be open ended.All
              dates in the JSON payloads are represented in ISO 8601 date-time
              format.

              All date-time field...

2. For transaction entries subject to availability/float and for which
      availability information is provided, the value date must not be used. In
      this case the availability component identifie...

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

#### GAP_0092: ATOM_151

**Requirement:** The Read Transaction Details endpoint SHALL be accessible via GET /v1/accounts/{account-id}/transactions/{transactionId}

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0101: ATOM_153

**Requirement:** The transactionId path parameter SHALL be given by the attribute transactionId of the corresponding entry of a transaction list

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0125: ATOM_160

**Requirement:** The Read Card Account List endpoint SHALL be accessible via GET /v1/card-accounts

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. ### Authorize a consent

The bank sends the request to the customer stating the accounts and information that the API consumer wishes to access.
    
       
  1. Generate the request object by signin...

</details>

---

#### GAP_0133: ATOM_161

**Requirement:** The Read Card Account Details endpoint SHALL be accessible via GET /v1/card-accounts/{account-id}

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. ### Authorize a consent

The bank sends the request to the customer stating the accounts and information that the API consumer wishes to access.
    
       
  1. Generate the request object by signin...

</details>

---

</details>

<details>
<summary><strong>Audit And Logging</strong> — 1 gap(s) | 1 not supported</summary>

### Audit And Logging

*1 gap(s) identified*

#### GAP_0102: ATOM_154

**Requirement:** The X-Request-ID header SHALL be mandatory and contain a UUID unique to the call as determined by the initiating party

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not explicitly enforce the `X-Request-ID` header as mandatory with a UUID unique to the call for all API endpoints...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not appear to explicitly support a mandatory `X-Request-ID` header with UUID validation as described in your q...

</details>

---

</details>

<details>
<summary><strong>Authentication</strong> — 41 gap(s) | 16 not supported | 23 partial | 2 unknown</summary>

### Authentication

*41 gap(s) identified*

#### GAP_0014: ATOM_165

**Requirement:** The system SHALL require X-Request-ID header as mandatory UUID for card account balance requests

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Writing a custom ID Token Builder

The default ID Token Builder in WSO2 Open Banking provides the pairwise subject calculation for authorization and token 
flow.

If the API consumer application su...

2. ## Writing a custom ID Token Builder

The default ID Token Builder in WSO2 Open Banking provides the pairwise subject calculation for authorization and token 
flow.

If the API consumer application su...

3. ### Account Information Service

If the API consumer application is aggregating account information on behalf of the bank user, the APP-to-APP redirection 
flow is as follows: 

[ ![](../assets/img/le...

</details>

---

#### GAP_0018: ATOM_166

**Requirement:** The system SHALL include PSU-IP-Address header conditionally when the request was actively initiated by the PSU

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

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

2. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support the conditional inclusion of a `PSU-IP-Address` header based on whether a request w...

3. [wso2-extensions/identity-inbound-auth-oauth]
[{'type': 'text', 'text': 'Error processing question: Repository not found. Visit https://deepwiki.com/wso2-extensions/identity-inbound-auth-oauth to inde...

</details>

---

#### GAP_0026: ATOM_099

**Requirement:** Authorization header SHALL be included when OAuth2 authentication was performed in a pre-step or during SCA

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

2. ## Client Authentication 

According to OAuth 2.0, the authorization server and the client need to establish a client authentication method that 
meets the security requirements of the authorization s...

3. ### setOauthAppProperties method
This method lets you enable OAuth 2.0 properties related to the application. For example, ID token encryption.

``` java
public void setOauthAppProperties(boolean isRe...

</details>

---

#### GAP_0029: ATOM_168

**Requirement:** The system SHALL include Authorization header conditionally only when OAuth2 based authentication was performed

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### setConditionalAuthScript method
This method lets you set a [conditional authentication script](https://is.docs.wso2.com/en/5.11.0/learn/using-opa-policies-for-adaptive-auth/#configure-the-adaptive...

2. ### getSubjectClaim method

This method contains the pairwise subject calculation logic. You can customize it according to your requirements. Given 
below is the method signature:

``` java
getSubject...

3. ### getSubjectClaim method

This method contains the pairwise subject calculation logic. You can customize it according to your requirements. Given 
below is the method signature:

``` java
getSubject...

</details>

---

#### GAP_0030: ATOM_141

**Requirement:** The system SHALL include PSU-IP-Address header when request was actively initiated by the PSU

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

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

2. [wso2/product-is]
[{'type': 'text', 'text': "This repository, `wso2/product-is`, does not directly support the explicit inclusion of a `PSU-IP-Address` header based on whether a request was actively i...

3. [wso2-extensions/identity-inbound-auth-oauth]
[{'type': 'text', 'text': 'Error processing question: Repository not found. Visit https://deepwiki.com/wso2-extensions/identity-inbound-auth-oauth to inde...

</details>

---

#### GAP_0032: ATOM_057

**Requirement:** The system MUST provide SCA process status information through 'scaStatus' data element in GET SCA Status Response Message for payment initiation.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. backendTime)`|`142`| In addition to the above-mentioned data elements, you can publish data that are specific to your open banking standard. For information on the additional data elements that you ca...

3. ### Step 2: Initiate a consent

In this step, the API consumer creates a request to get the consent of the customer to access the accounts and its 
information from the bank. 

A sample consent initia...

</details>

---

#### GAP_0036: ATOM_107

**Requirement:** The Authorization header SHALL be included only when OAuth2 based authentication was performed in a pre-step or current transaction

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

2. ### setConditionalAuthScript method
This method lets you set a [conditional authentication script](https://is.docs.wso2.com/en/5.11.0/learn/using-opa-policies-for-adaptive-auth/#configure-the-adaptive...

3. ### doPreCreateApplication method

This method lets you change the `oAuthAppRequest` before the application creation.

``` java
/**
* Do changes to app request before creating the app at toolkit level...

</details>

---

#### GAP_0043: ATOM_019

**Requirement:** The API SHALL support dedicated authorisation endpoints for payment initiation and consent establishment to handle transaction authorisation by PSUs starting from version 1.2

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## How WSO2 Open Banking Accelerator delivers open banking requirements 1. **API Consumer Onboarding** - API consumer onboarding is the process of verifying an API consumer when they register with a b...

2. ### Step 3: Authorizing a consent

The API consumer application redirects the bank customer to authenticate and approve/deny application-provided consents.

1. Generate a request object by signing you...

3. ### Step 3: Authorizing a consent

The API consumer application redirects the bank customer to authenticate and approve/deny application-provided consents.

1. Generate a request object by signing you...

</details>

---

#### GAP_0046: ATOM_090

**Requirement:** ASPSP SHALL return ASPSP-SCA-Approach header with value 'DECOUPLED' when PSU chooses decoupled authentication method in embedded flow

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

3. #Client-Initiated Backchannel Authentication (CIBA) Flow

WSO2 Open Banking Accelerator provides support for the
[OpenID Connect Client-Initiated Backchannel Authentication Flow](https://openid.net/sp...

</details>

---

#### GAP_0047: ATOM_059

**Requirement:** The system MUST support payment initiation transaction status 'PATC' (PartiallyAcceptedTechnicalCorrect) for multilevel SCA when at least one PSU has authorized but final authorization is pending.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

3. ## Consent Authorization

- Once you enter a properly constructed authorization request in your web browser, based on the `bank_code` in the 
  request object, you will be redirected to ABC bank or DC...

</details>

---

#### GAP_0050: ATOM_204

**Requirement:** The client_id parameter shall contain the organizationIdentifier from the eIDAS certificate in the format 'PSD[2-char-country]-[NCA-identifier]-[PSP-identifier]'

- **Strength:** `SHALL`
- **Section:** `13.1`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### getKeyId method

The method contains the KeyID calculation logic. You can customize it according to your requirements. Given below is 
the method signature:

``` java
public String getKeyId(Certif...

3. ## Configuring a custom CIBA Authentication Endpoint Consent Updater  

1. Once implemented, build a JAR file for your project.
2. Place the above-created JAR file in the `<IS_HOME>/repository/compone...

</details>

---

#### GAP_0054: ATOM_173

**Requirement:** The system SHALL create authorisation sub-resource via POST to authorisation endpoints and return HTTP 201 status code

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### postProcessRequest method

This method handles the requests after API Authentication.

``` java
public void postProcessRequest(OBAPIRequestContext obapiRequestContext);
```

2. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

3. ### Dynamic Endpoint Policy

Dynamic Endpoint Policy is a policy designed to be engaged in the request flow of any request that requires to be routed to the consent manage service or the actual backen...

</details>

---

#### GAP_0059: ATOM_174

**Requirement:** The system SHALL return mandatory scaStatus and authorisationId in authorisation creation response

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Persist

The second extension point of the Consent Authorize component is the Persist Flow. The Persistent functionality is engaged once the 
user approves/denies the consent via an API invocation ...

2. ## How WSO2 Open Banking Accelerator delivers open banking requirements 1. **API Consumer Onboarding** - API consumer onboarding is the process of verifying an API consumer when they register with a b...

3. 6. After the user approves/denies the consent and selects the accounts, a `PATCH authorize/persist` request is made to persist the consent information. 7. Finally, if the persistence is successful, to...

</details>

---

#### GAP_0060: ATOM_115

**Requirement:** For multilevel SCA payments, the API SHALL require explicit start of authorization and not contain direct SCA processing links in payment initiation response

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. reference: ``` [open_banking.push_authorisation] expiry_time=60 request_uri_sub_string="substring" ``` !!! note You can change the format of the request_uri using the `request_uri_sub_string` tag. ```...

3. ## Writing a custom Gateway Executor

The WSO2 Open Banking Accelerator contains extension points known as Open Banking Executors that can validate and 
manipulate API requests. The executors can medi...

</details>

---

#### GAP_0061: ATOM_011

**Requirement:** Electronic signatures SHALL be included in HTTP header as defined by signHTTP specification chapter 4.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. A pushed authorization request contains authentication and authorization request parameters, which will be used in the Pushed Authorization endpoint of WSO2 Open Banking Accelerator. The Pushed Author...

3. ### Step 3: Authorizing a consent

The API consumer application redirects the bank customer to authenticate and approve/deny application-provided consents.

1. Generate a request object by signing you...

</details>

---

#### GAP_0062: ATOM_175

**Requirement:** The system SHALL include ASPSP-SCA-Approach header conditionally in authorisation responses with values EMBEDDED, DECOUPLED, or REDIRECT

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### setConditionalAuthScript method
This method lets you set a [conditional authentication script](https://is.docs.wso2.com/en/5.11.0/learn/using-opa-policies-for-adaptive-auth/#configure-the-adaptive...

3. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

</details>

---

#### GAP_0068: ATOM_176

**Requirement:** The system SHALL support TPP-Redirect-URI header for redirect SCA approach when TPP-Redirect-Preferred equals true

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

3. ## How WSO2 Open Banking supports App-to-App redirection [ ![](../assets/img/learn/app-to-app-redirection/app-to-app-redirection-sequence-flow.png) ](../assets/img/learn/app-to-app-redirection/app-to-...

</details>

---

#### GAP_0069: ATOM_089

**Requirement:** ASPSP SHALL support mixed SCA approaches allowing PSU to choose decoupled authentication method even when flow starts with redirect approach

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. #Client-Initiated Backchannel Authentication (CIBA) Flow

WSO2 Open Banking Accelerator provides support for the
[OpenID Connect Client-Initiated Backchannel Authentication Flow](https://openid.net/sp...

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

#### GAP_0073: ATOM_119

**Requirement:** Account Information Service consent SHALL be authorised by the PSU towards the ASPSP with Strong Customer Authentication as mandated by EBA-RTS

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## How to manage consents

The API consumer applications seek consent from their customers who wish to expose their financial data through the 
application. When granting consent the customers must kn...

2. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

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

#### GAP_0074: ATOM_081

**Requirement:** OAuth2 based authentication SHALL be supported as a pre-step for PSU authentication in payment initiation flows

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. **Consumer Authentication** is a mechanism used to authenticate a user that initiates a payment or accesses banking 
information via an API consumer application. Authentication can be configured using...

2. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

3. The TPPs can create OAuth 2.0 client applications to facilitate banking services exposed via Bank APIs. WSO2 Open Banking provides the Client Registration feature to register the applications in the b...

</details>

---

#### GAP_0075: ATOM_177

**Requirement:** The system SHALL update PSU identification data via PUT requests to authorisation sub-resources and return HTTP 200

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

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

2. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support updating "PSU identification data via PUT requests to authorisation sub-resources" ...

3. [wso2-extensions/identity-inbound-auth-oauth]
[{'type': 'text', 'text': 'Error processing question: Repository not found. Visit https://deepwiki.com/wso2-extensions/identity-inbound-auth-oauth to inde...

</details>

---

#### GAP_0076: ATOM_091

**Requirement:** Multilevel SCA SHALL support authorization of payments by multiple users using explicit start of authorization mechanisms

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. ## Stakeholders in Open Banking / Open Finance
   
The open banking ecosystem comprises 4 main stakeholders.
   
   * **Customer** - The owner of a bank account who can grant access to the API consume...

3. reference: ``` [open_banking.push_authorisation] expiry_time=60 request_uri_sub_string="substring" ``` !!! note You can change the format of the request_uri using the `request_uri_sub_string` tag. ```...

</details>

---

#### GAP_0080: ATOM_087

**Requirement:** ASPSP SHALL provide list of available SCA methods to TPP when multiple authentication methods are supported for the PSU

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

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

2. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

3. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

</details>

---

#### GAP_0086: ATOM_021

**Requirement:** The API SHALL support signing of a group of transactions with one SCA process

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## How WSO2 Open Banking Accelerator delivers open banking requirements 1. **API Consumer Onboarding** - API consumer onboarding is the process of verifying an API consumer when they register with a b...

2. ISO 20022). - mediation between a legacy or digital core and other banking systems, and the bank’s library of open banking APIs. 6. **Data Analytics** - The solution to mediate between the bank’s syst...

3. ### Step 3: Authorizing a consent

The API consumer application redirects the bank customer to authenticate and approve/deny application-provided consents.

1. Generate a request object by signing you...

</details>

---

#### GAP_0091: ATOM_181

**Requirement:** In case of incorrect password, the TPP needs to ask the PSU for re-entering the password and the newly entered password needs to be updated to the same path.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0096: ATOM_020

**Requirement:** The API SHALL support multiple level SCA where a transaction needs authorisation by more than one PSU in corporate contexts

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ISO 20022). - mediation between a legacy or digital core and other banking systems, and the bank’s library of open banking APIs. 6. **Data Analytics** - The solution to mediate between the bank’s syst...

2. ## Open banking / Open Finance regulations Open banking and Open Finance regulations provide a policy and legislative framework to help banks and API consumers deliver the benefits of open banking. - ...

3. ## Stakeholders in Open Banking / Open Finance
   
The open banking ecosystem comprises 4 main stakeholders.
   
   * **Customer** - The owner of a bank account who can grant access to the API consume...

</details>

---

#### GAP_0109: ATOM_078

**Requirement:** The ASPSP must validate Client ID, Redirect URI, and TPP Role in OAuth2 SCA approach

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

3. ## Client Authentication 

According to OAuth 2.0, the authorization server and the client need to establish a client authentication method that 
meets the security requirements of the authorization s...

</details>

---

#### GAP_0114: ATOM_157

**Requirement:** The Authorization header SHALL be included only if OAuth2 based authentication or SCA was performed

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Client Authentication 

According to OAuth 2.0, the authorization server and the client need to establish a client authentication method that 
meets the security requirements of the authorization s...

2. ## Authorization Request

Before a third-party API consumer application accesses the customer's banking information, the API consumer sends an 
authorization request to get the customer's consent for ...

3. ### setOauthAppProperties method
This method lets you enable OAuth 2.0 properties related to the application. For example, ID token encryption.

``` java
public void setOauthAppProperties(boolean isRe...

</details>

---

#### GAP_0117: ATOM_113

**Requirement:** The TPP-Redirect-URI header SHALL be mandatory for Redirect SCA Approach when TPP-Redirect-Preferred equals true

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### Step 1: Sign up as a TPP

1. Go to the Developer portal at `https://<APIM_HOST>:9443/devportal`.

2. Go to the **Applications** tab. <br/> ![applications_tab](../../assets/img/learn/mcr/applicatio...

3. ### Step 2: Sign in to the Developer Portal as the TPP

1. Now, sign in to the [Developer portal](https://<APIM_HOST>:9443/devportal) as the TPP.

2. Enter the username and the password you entered wh...

</details>

---

#### GAP_0121: ATOM_084

**Requirement:** ASPSP SHALL return HTTP status code 201 (Created) when credentials are validated successfully in Start Authorization Response

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### postProcessRequest method

This method handles the requests after API Authentication.

``` java
public void postProcessRequest(OBAPIRequestContext obapiRequestContext);
```

2. ### preProcessRequest method

This method handles the requests before API Authentication.

``` java
public void preProcessRequest(OBAPIRequestContext obapiRequestContext);
```

3. ### setAuthenticators method
This method lets you configure authenticators to be invoked during the authorization flow.

``` java
public void setAuthenticators (boolean isRegulatoryApp, String tenantD...

</details>

---

#### GAP_0123: ATOM_083

**Requirement:** TPP MUST provide PSU credentials (User-ID and Password) in the Start Authorization Request body for embedded SCA approach

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

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

3. ### Step 5: Generate keys

The TPP application requires a Client ID (Consumer Key) to access the subscribed API.

1. Go to the **Applications** tab in the Developer Portal.

2. From the application li...

</details>

---

#### GAP_0130: ATOM_085

**Requirement:** ASPSP SHALL provide SCA challenge data (e.g. Photo OTP bitmap) in Authorization Response when only one SCA method is available

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ##Writing a custom claim provider

The `OBClaimProvider` class is an extension that lets you customize and create your own claim provider and add 
additional claims to the authorization and/or token r...

2. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

3. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

</details>

---

#### GAP_0134: ATOM_074

**Requirement:** The ASPSP must validate request syntax and TPP role semantics during payment initiation

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

3. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

</details>

---

#### GAP_0136: ATOM_086

**Requirement:** TPP MUST submit OTP authentication data in Authorization-Update Request body when responding to SCA challenge

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. ### Step 5: Generate keys

The TPP application requires a Client ID (Consumer Key) to access the subscribed API.

1. Go to the **Applications** tab in the Developer Portal.

2. From the application li...

</details>

---

#### GAP_0141: ATOM_092

**Requirement:** Multiple SCA processes in multilevel authorization MAY be performed simultaneously

- **Strength:** `MAY`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. as a Java Map in the Worker Java implementation. You can use these properties to implement the logic you want. 3. Worker Name - This is the name of the Worker. !!! note Provide the same name you confi...

2. ## Writing a custom Gateway Executor

The WSO2 Open Banking Accelerator contains extension points known as Open Banking Executors that can validate and 
manipulate API requests. The executors can medi...

3. ## Configuring a custom Push Authenticator  

1. Once implemented, build a JAR file for your project.
2. Place the above-created JAR file in the `<IS_HOME>/repository/components/dropins` directory.
3....

</details>

---

#### GAP_0143: ATOM_203

**Requirement:** OAuth2 response type 'code' is recommended for authorization requests

- **Strength:** `RECOMMENDED`
- **Section:** `13.1`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** unknown
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. # supported types : Basic-Auth or OAuth2
type = "Basic-Auth"
username = ""
password = ""
```

2. # supported types : Basic-Auth or OAuth2
type = "Basic-Auth"
username = ""
password = ""
```

3. # supported types : Basic-Auth or OAuth2
type = "Basic-Auth"
username = ""
password = ""
```

</details>

---

#### GAP_0148: ATOM_022

**Requirement:** ASPSPs MAY offer a signing-baskets endpoint to support grouping of several transactions for common authorisation process

- **Strength:** `MAY`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

2. ## Java based extensions (Old approach)

- [Open Banking Gateway](open-banking-gateway.md)
- [Open Banking Event Executor](custom-event-executor.md)
- [Data Publishing](authentication-flow-for-data-pu...

3. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

</details>

---

#### GAP_0150: ATOM_088

**Requirement:** TPP SHOULD filter available SCA methods if not all authentication methods can be technically supported

- **Strength:** `SHOULD`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. ### Software Statement Assertion (SSA)

A software statement that is signed by its issuer is referred to as an SSA. An SSA is represented as a JSON Web Signature (JWS). An SSA is unique for an applica...

3. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

</details>

---

#### GAP_0155: ATOM_023

**Requirement:** ASPSPs MAY restrict transaction grouping in signing baskets to payments only, individual payments only, or same payment product only

- **Strength:** `MAY`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** unknown
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Payment Initiation Service

If the API consumer application is initiating a credit transfer on behalf of the bank customer, the App-to-App redirection 
flow is as follows:

[ ![](../assets/img/lea...

2. ### Account Information Service

If the API consumer application is aggregating account information on behalf of the bank user, the APP-to-APP redirection 
flow is as follows: 

[ ![](../assets/img/le...

3. ## Stakeholders in Open Banking / Open Finance
   
The open banking ecosystem comprises 4 main stakeholders.
   
   * **Customer** - The owner of a bank account who can grant access to the API consume...

</details>

---

#### GAP_0156: ATOM_079

**Requirement:** The ASPSP should provide PSU message to inform about decoupled authentication requirement

- **Strength:** `SHOULD`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

</details>

---

#### GAP_0160: ATOM_010

**Requirement:** The ASPSP MAY require the TPP to sign request messages using qualified certificates for electronic seals.

- **Strength:** `MAY`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Dynamic Client Registration

With the Open Banking OpenID Dynamic Client Registration API, TPPs can register with ASPSPs in a seamless and a fully automated basis. To use DCR, a TPP has to register...

2. ## Manual Client Registration

Manual Client Registration or Signup Workflow is the process of on boarding the TPPs through the Dev Portal Signuo process. In this method, you can configure workflows t...

3. swagger: '2.0'
info:
  title: DynamicClientRegistrationAPI
  description: >
    This specification defines the APIs for a TPP to submit a Software Statement
    Assertion to an ASPSP for the purpose o...

</details>

---

</details>

<details>
<summary><strong>Certificate Management</strong> — 12 gap(s) | 2 not supported | 10 partial</summary>

### Certificate Management

*12 gap(s) identified*

#### GAP_0016: ATOM_005

**Requirement:** The TPP certificate content SHALL be compliant with EBA-RTS requirements.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports aspects related to certificate handling, particularly within the context of OAuth2 and JWKS endpoints. While t...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, provides functionalities for managing client and endpoint certificates, but it does not explicitly support or valid...

</details>

---

#### GAP_0037: ATOM_201

**Requirement:** The TPP-Signature-Certificate header shall contain the TPP's eIDAS certificate

- **Strength:** `SHALL`
- **Section:** `4e52743eb3ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the handling of certificates, including the ability to update and retrieve them for Identity Provide...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support the use of client certificates, which could be relevant to the `TPP-Signature-Certificate` heade...

</details>

---

#### GAP_0063: ATOM_026

**Requirement:** TPPs SHALL be identified using PSD2 related eIDAS certificates as specified in ETSI PSD2 standards

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the identification of Third-Party Providers (TPPs) using eIDAS certificates, specifically for Financial-grade ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to have some capabilities related to certificate management, which might be relevant to the identification ...

</details>

---

#### GAP_0065: ATOM_094

**Requirement:** TPP registration information including TPP Number, TPP Name, TPP Roles, and National Competent Authority MUST be validated from eIDAS certificates

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support X.509 certificate authentication, which is a prerequisite for eIDAS certificate validation. Specific...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, this repository, `wso2/product-apim`, appears to handle JWT (JSON Web Token) validation and identity provider manage...

</details>

---

#### GAP_0089: ATOM_180

**Requirement:** The certificate used for signing the request must be provided in base64 encoding in the TPP-Signature-Certificate header field.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the handling of base64 encoded certificates, which is relevant to the `TPP-Signature-Certificate` header field...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports the use of base64 encoded certificates for signing requests, particularly in the context of mutual SSL and...

</details>

---

#### GAP_0094: ATOM_082

**Requirement:** eIDAS certificate validation SHALL be performed for all payment initiation requests including certificate, request syntax, TPP role and semantics verification

- **Strength:** `SHALL`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports certificate validation, including the handling of JWKS URIs and direct certificate uploads for Identity Provid...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support mutual SSL certificate validation, which is a foundational component for eIDAS certificate valid...

</details>

---

#### GAP_0112: ATOM_187

**Requirement:** The keyId field in the Signature header must be the serial number of the TPP's certificate included in the TPP-Signature-Certificate header

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the validation of the `keyId` field in the Signature header against the serial number of a certifica...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support the verification of the `keyId` field in a JWT header against a JWKS endpoint, but not specifica...

</details>

---

#### GAP_0118: ATOM_188

**Requirement:** The keyId must be formatted as keyId="SN=XXX,CA=YYYYYYYYYYYYYYYY" where XXX is the certificate serial number in hexadecimal and YYYYYYYYYYYYYYYY is the full Distinguished Name of the Certification Authority

- **Strength:** `SHALL`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support the `keyId` format `keyId="SN=XXX,CA=YYYYYYYYYYYYYYYY"` where `XXX` is the certific...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support the `keyId` format `keyId="SN=XXX,CA=YYYYYYYYYYYYYYYY"` through its WS-SecurityPolicy configurat...

</details>

---

#### GAP_0124: ATOM_072

**Requirement:** ASPSPs SHALL validate eIDAS certificate, request syntax, TPP role, and semantics during payment initiation

- **Strength:** `SHALL`
- **Section:** `648825991d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support aspects of eIDAS certificate validation and TPP role authorization, particularly within the context ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, this repository, `wso2/product-apim`, appears to offer functionalities related to managing client and endpoint certi...

</details>

---

#### GAP_0127: ATOM_073

**Requirement:** The ASPSP must validate the eIDAS certificate for payment initiation requests in redirect SCA approach

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, WSO2 Identity Server, appears to support certificate validation, which is a prerequisite for eIDAS certificate validation. Specifically, i...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support certificate validation, including certificate chain validation and revocation checks, which are ...

</details>

---

#### GAP_0131: ATOM_004

**Requirement:** The TPP SHALL use a qualified certificate for website authentication issued by a qualified trust service provider according to eIDAS regulation.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the use of X.509 certificates for website authentication, which is a foundational component for impl...

2. [wso2/product-apim]
[{'type': 'text', 'text': '# Answer\n\nBased on my review of the codebase, **this repository does not contain explicit support for eIDAS-compliant qualified certificates for TPP (T...

</details>

---

#### GAP_0137: ATOM_006

**Requirement:** The TPP certificate SHALL indicate all roles the TPP is authorised to use.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the management of roles within Identity Providers (IdPs) and can be configured to handle role claims, which co...

2. [wso2/product-apim]
[{'type': 'text', 'text': "I appreciate your question, but I need to clarify what you're asking about. Based on the codebase context provided (which is from `wso2/product-apim` - W...

</details>

---

</details>

<details>
<summary><strong>Consent Management</strong> — 17 gap(s) | 2 not supported | 13 partial | 2 unknown</summary>

### Consent Management

*17 gap(s) identified*

#### GAP_0002: ATOM_118

**Requirement:** Account Information Service SHALL enforce the multiplicity of access (one-off or recurring) as specified in the consent

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### amendConsentData method

This method lets you amend the consent receipt or validity period. It is mandatory to provide the consent ID with 
either the consent receipt or validity period. When the ...

2. #### Add CustomerCareOfficerRole Role

CustomerCareOfficerRole is required for bank users to log into the Consent Manager Portal and search for the consents granted by any user.

1. Go to **Roles** un...

3. ## Shareable and payable accounts 
   
Some bank customers may have a certain number of bank accounts in a particular bank, but not all these accounts have 
the ability to be shared externally or to m...

</details>

---

#### GAP_0004: ATOM_131

**Requirement:** ASPSP SHALL offer consent extension for both Detailed and Global Consent models if offered for one of these models

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** unknown
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## Setting up Consent manager app

2. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

3. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

</details>

---

#### GAP_0007: ATOM_062

**Requirement:** The system MUST support consent status 'revokedByPsu' when consent has been revoked by the PSU.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### revokeConsent method

This method lets you revoke a consent by performing the following: 

 - Retrieves the consent for status validation
 - Updates the existing status of the consent
 - Creates a...

2. ### Revoking a consent

- To revoke a consent, review the details and click **Stop Sharing**. 
    
    ![consent details](../assets/img/learn/consent-manager/stop-sharing.png)
    
- Revoking a conse...

3. ### revokeExistingApplicableConsents method

This method lets you revoke existing consents for a given combination of `clientID`, `userID`, `consent type`, and 
`status` parameters. It also revokes an...

</details>

---

#### GAP_0008: ATOM_164

**Requirement:** The system SHALL ensure account-id remains constant at least throughout the lifecycle of a given consent

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. ## **Usage** **>> consent-cleanup.sql** This is a consent data cleanup script with batch wise delete, This procedure includes the cleanup of consents from the respective tables of *FS_CONSENT* , *FS_C...

</details>

---

#### GAP_0011: ATOM_061

**Requirement:** The system MUST support consent status 'expired' when consent has exceeded its validity period such as 90 days.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

2. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

3. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

</details>

---

#### GAP_0023: ATOM_167

**Requirement:** The system SHALL require Consent-ID header as mandatory for card account balance requests

- **Strength:** `SHALL`
- **Section:** `feec7d26c6c6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Step 3: Authorizing a consent

The API consumer application redirects the bank customer to authenticate and approve/deny application-provided consents.

1. Generate a request object by signing you...

2. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

3. ### Step 3: Authorizing a consent

The API consumer application redirects the bank customer to authenticate and approve/deny application-provided consents.

1. Generate a request object by signing you...

</details>

---

#### GAP_0070: ATOM_137

**Requirement:** The system SHALL validate that Consent-ID header is provided as mandatory for account details requests

- **Strength:** `SHALL`
- **Section:** `fcc6292f816f`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

2. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

3. ### amendConsentData method

This method lets you amend the consent receipt or validity period. It is mandatory to provide the consent ID with 
either the consent receipt or validity period. When the ...

</details>

---

#### GAP_0079: ATOM_031

**Requirement:** The ASPSP SHALL provide a mandatory POST consents endpoint to create a consent resource defining access rights to dedicated accounts of a given PSU-ID

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Data
The following table explains the data available in `ConsentValidateData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| headers ...

2. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

3. ### createExclusiveConsent method

This method lets you create an exclusive consent by performing the following:

 - Updates existing consent statuses and deactivate their account mappings
 - Creates ...

</details>

---

#### GAP_0083: ATOM_063

**Requirement:** The system MUST support consent status 'terminatedByTpp' when AIS has terminated the consent.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

2. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

3. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

</details>

---

#### GAP_0085: ATOM_032

**Requirement:** The ASPSP SHALL provide a mandatory GET consents/{consentId} endpoint to read the exact definition of the given consent resource including validity status

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### getConsent method

This method lets you retrieve a consent with or without its attributes by performing the following: 

- Retrieves the consent for status validation
- Optionally retrieves consen...

2. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

3. ### amendConsentData method

This method lets you amend the consent receipt or validity period. It is mandatory to provide the consent ID with 
either the consent receipt or validity period. When the ...

</details>

---

#### GAP_0087: ATOM_123

**Requirement:** ASPSP SHALL deny access for one-off consent if AISP requests data more than once or if consent validity has timed out

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
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

#### GAP_0090: ATOM_033

**Requirement:** The ASPSP SHALL provide a mandatory DELETE consents/{consentId} endpoint to terminate the addressed consent

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
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

#### GAP_0095: ATOM_117

**Requirement:** Account Information Service SHALL grant access based on the type of Account Information Service specified in the consent

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. #### Add CustomerCareOfficerRole Role

CustomerCareOfficerRole is required for bank users to log into the Consent Manager Portal and search for the consents granted by any user.

1. Go to **Roles** un...

2. ## Using Consent Manager

1. Go to the Consent Manager application at `https://<IS_HOST>:9446/consentmgr`.

2. Sign in with the credentials of the users created in [Create Users](../learn/consent-mana...

3. ### Viewing consent details

- To view consent details, click the respective `Action` button. 

    ![view consent](../assets/img/learn/consent-manager/view-consent.png)

- You can view the details su...

</details>

---

#### GAP_0104: ATOM_156

**Requirement:** The Consent-ID header SHALL be mandatory for transaction detail requests

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

2. ### Data 
The following table explains the data available in `ConsentRetrieveData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| session...

3. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

</details>

---

#### GAP_0105: ATOM_128

**Requirement:** ASPSP SHALL support Global Consent model where TPP submits only PSU identification for general account access

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Data
The following table explains the data available in `ConsentValidateData`.

| Name      | Type                  | Description  |
| ----------|-----------------------| -------------|
| headers ...

2. ## Consent REST API
    
When interacting with the consent module, you can use the [Consent REST API](../references/consent-rest-api.md) exposed 
by WSO2 Open Banking Accelerator.

3. components:
  schemas:
    ConsentValidateDetail:
      type: object
      properties:
        headers:
          description: Object containing keys and values of request headers received to the gate...

</details>

---

#### GAP_0129: ATOM_060

**Requirement:** The system MUST support consent status values 'received', 'rejected', and 'valid' during the AIS consent initiation phase.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** unknown
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. ### Consent Enforcement Policy

Consent Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires the consent to be validated prior to an API resource call...

2. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

3. ### Error Handling
In any of the consent extensions, if an error scenario occurs and you need to send an error response make sure to throw 
a `ConsentException`.

</details>

---

#### GAP_0159: ATOM_130

**Requirement:** ASPSP MAY require an explicit consent extension by the PSU to deliver the account owner name

- **Strength:** `MAY`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

</details>

<details>
<summary><strong>Data Access</strong> — 8 gap(s) | 2 not supported | 6 partial</summary>

### Data Access

*8 gap(s) identified*

#### GAP_0009: ATOM_028

**Requirement:** All API methods addressing dynamically created resources SHALL only apply to resources created by the same TPP

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the requirement that API methods addressing dynamically created resources only apply to resources created by t...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports the requirement that API methods addressing dynamically created resources only apply to resources created ...

</details>

---

#### GAP_0021: ATOM_125

**Requirement:** ASPSP SHALL deny access if the actual access does not match the consented duration or frequency

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports consent management, which includes the ability to define and enforce consent for sharing user attributes with ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Yes, this repository supports denying access if the actual access does not match the consented duration or frequency through its throttling mechanisms.  ...

</details>

---

#### GAP_0024: ATOM_014

**Requirement:** ASPSPs SHALL accept at minimum the basic character set including letters, numbers, and specified symbols.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports character set validation for usernames and other fields through regular expressions defined in configuration f...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, demonstrates support for a basic character set in various contexts, including API resource names, endpoint security...

</details>

---

#### GAP_0028: ATOM_126

**Requirement:** ASPSP SHALL check access frequency per account that has been accessed and per PSU for list of accounts consent

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support checking access frequency per account and per PSU for list of accounts consent. The...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, WSO2 API Manager, supports rate limiting and throttling policies that can be applied to APIs.  These policies can control API usage base...

</details>

---

#### GAP_0067: ATOM_016

**Requirement:** Resources SHALL be addressed under API endpoints using the format https://{provider}/v1/{service}{?query-parameters}.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Yes, the WSO2 Identity Server repository supports the API endpoint format `https://{provider}/v1/{service}{?query-parameters}`. This structure is evident a...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports API endpoints that generally conform to a structure similar to `https://{provider}/v1/{service}{?query-par...

</details>

---

#### GAP_0084: ATOM_124

**Requirement:** ASPSP SHALL deny access if the requested Account Information Service type does not comply with the consented service

- **Strength:** `SHALL`
- **Section:** `2035ed10aab6`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports denying access if the requested Account Information Service type does not comply with the consented service th...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, WSO2 API Manager, supports denying access if the requested Account Information Service (AIS) type does not comply with the consented ser...

</details>

---

#### GAP_0099: ATOM_007

**Requirement:** Message parameters SHALL be encoded in spinal-case (small letters) on path level.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, primarily uses SCIM 2.0 for its User APIs, and the SCIM 2.0 specification generally uses camelCase for its attributes a...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, the repository does not explicitly enforce or support spinal-case formatting for path parameters. The OpenAPI/Swagge...

</details>

---

#### GAP_0126: ATOM_008

**Requirement:** Message parameters SHALL be encoded in Spinal-case (starting capital letters) on HTTP header level.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not explicitly enforce or support Spinal-case formatting for HTTP header parameters. The provided code snippets pr...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not explicitly enforce or provide configuration options for HTTP header parameters to be encoded in Spinal-cas...

</details>

---

</details>

<details>
<summary><strong>Error Handling</strong> — 7 gap(s) | 2 not supported | 5 partial</summary>

### Error Handling

*7 gap(s) identified*

#### GAP_0006: ATOM_040

**Requirement:** The ASPSP SHALL include mandatory messageCode field in additional error information responses

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the inclusion of a `code` field in additional error information responses. The `code` field is a mandatory com...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports the inclusion of a `code` field in error responses. The OpenAPI specifications for various APIs within thi...

</details>

---

#### GAP_0027: ATOM_042

**Requirement:** Error responses must include a structured JSON format with type, title, detail, code, and optional additionalErrors fields.

- **Strength:** `MUST`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Yes, the WSO2 Identity Server repository supports structured JSON error responses that include `code`, `message`, and `description` fields, and in some cas...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Yes, the repository supports structured JSON error responses with `code`, `message`, `description`, `moreInfo`, and an `error` array for additional error...

</details>

---

#### GAP_0077: ATOM_036

**Requirement:** The ASPSP SHALL return HTTP response code 201 for successful POST requests where Payment Initiation or Consent Request was correctly performed

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports returning an HTTP `201 Created` status code for successful `POST` requests related to certain resource creatio...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support returning an HTTP 201 status code for successful POST requests across various API operations, in...

</details>

---

#### GAP_0097: ATOM_043

**Requirement:** Error responses must use Content-Type application/problem+json header.

- **Strength:** `MUST`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not explicitly support the `Content-Type: application/problem+json` header for error responses based on the provid...

2. [wso2/product-apim]
[{'type': 'text', 'text': "Based on the provided codebase, the repository does not explicitly support the `Content-Type: application/problem+json` header for error responses. Inste...

</details>

---

#### GAP_0120: ATOM_035

**Requirement:** The ASPSP SHALL return HTTP response code 200 for successful PUT and GET requests, including repeated requests due to timeout

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support returning HTTP 200 for successful PUT and GET requests, including in scenarios that might involve re...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, demonstrates support for returning HTTP 200 status codes for successful PUT and GET requests, including scenarios t...

</details>

---

#### GAP_0154: ATOM_182

**Requirement:** It is recommended that the ASPSP inform the TPP about incorrect password by adding a _links section in the additional error information and presenting a corresponding updatePsuAuthentication or updateEncryptedPsuAuthentication hyperlink.

- **Strength:** `SHOULD`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support the specific Open Banking requirement of informing the TPP about incorrect password...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not appear to directly support the specific requirement of informing a TPP about an incorrect password by addi...

</details>

---

#### GAP_0161: ATOM_039

**Requirement:** The ASPSP MAY communicate additional error information using tppMessageInformation with category set to ERROR when 4xx or 5xx HTTP response codes occur

- **Strength:** `MAY`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': "This repository, `wso2/product-is`, supports communicating additional error information when 4xx or 5xx HTTP response codes occur, but it does not explicit...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports communicating additional error information with 4xx or 5xx HTTP response codes. The error responses are ty...

</details>

---

</details>

<details>
<summary><strong>Funds Confirmation</strong> — 5 gap(s) | 4 not supported | 1 partial</summary>

### Funds Confirmation

*5 gap(s) identified*

#### GAP_0034: ATOM_034

**Requirement:** The ASPSP SHALL provide a mandatory POST funds-confirmations endpoint to check whether a specific amount is available at point of time of the request on an account

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to directly support a mandatory `POST /funds-confirmations` endpoint for checking fund availability on ...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to be an API Management platform. While it supports the creation and management of APIs, including defining...

</details>

---

#### GAP_0064: ATOM_102

**Requirement:** Payment status response SHALL include fundsAvailable field when funds check was performed and transaction status is ACTC, ACWC, or ACCP

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'Based on the provided codebase context, there is no information or code that directly supports the requirement for a payment status response to include a `...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, specifically within the `wso2/product-apim` project, does not appear to directly support the requirement of including a `fundsAvailable`...

</details>

---

#### GAP_0071: ATOM_207

**Requirement:** The scope parameter shall reference the consent resource in the format 'PIIS:<consentId>' for Payment Instrument Issuer Services

- **Strength:** `SHALL`
- **Section:** `13.1`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the concept of scopes in OAuth2/OpenID Connect, including custom scopes and consent management. Howe...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to have some support for managing scopes, which are relevant to the `scope` parameter in API calls. However...

</details>

---

#### GAP_0078: ATOM_051

**Requirement:** The system MUST support payment initiation transaction status 'ACFC' (AcceptedFundsChecked) when funds availability has been verified positively in addition to customer profile.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': "Based on the provided codebase, there is no direct support for the payment initiation transaction status 'ACFC' (AcceptedFundsChecked) or any explicit mech...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not appear to directly support the payment initiation transaction status \'ACFC\' (AcceptedFundsChecked) as de...

</details>

---

#### GAP_0151: ATOM_055

**Requirement:** The system MAY provide optional 'fundsAvailable' boolean data element in GET Status Response Message for ASPSPs not booking money directly from account.

- **Strength:** `MAY`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': "Based on the provided codebase, there is no direct support for an optional `fundsAvailable` boolean data element in GET Status Response Messages for ASPSPs...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not appear to directly support the specific `fundsAvailable` boolean data element in GET Status Response Messa...

</details>

---

</details>

<details>
<summary><strong>General</strong> — 6 gap(s) | 1 not supported | 4 partial | 1 unknown</summary>

### General

*6 gap(s) identified*

#### GAP_0031: ATOM_095

**Requirement:** X-Request-ID header MUST be included in all payment initiation API calls as unique request identifier

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to have some support for "payment initiation" as a type of authorization detail, but there is no direct evidenc...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'Based on the provided code snippets, this repository, `wso2/product-apim`, does not explicitly support an `X-Request-ID` header for payment initiation AP...

</details>

---

#### GAP_0056: ATOM_064

**Requirement:** The system MUST provide hyperlinks with semantic tags in '_links' data element to enable API steering for payment initiation and account information services.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the inclusion of hyperlinks with semantic tags in `_links` data elements within API responses, which can be us...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to have some support for handling hyperlinks and links within its registry system, but there is no direct e...

</details>

---

#### GAP_0088: ATOM_149

**Requirement:** API responses MUST include proper HTTP headers including X-Request-ID and Content-Type

- **Strength:** `MUST`
- **Section:** `f30dd2c91d5e`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support the inclusion of `Content-Type` headers in API responses, but there is no explicit evidence in the p...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support the inclusion of `Content-Type` and `Last-Modified` headers in API responses, and in some cases,...

</details>

---

#### GAP_0115: ATOM_065

**Requirement:** The system MUST include location header containing link to created resource in payment initiation and consent request responses.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the inclusion of a `Location` header containing a link to the created resource in responses for resource creat...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports the inclusion of a `Location` header containing a link to the created resource in responses for various re...

</details>

---

#### GAP_0147: ATOM_067

**Requirement:** The system MAY add additional data attributes to response messages and MUST document such extensions in ASPSP XS2A interface documentation.

- **Strength:** `MAY`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the addition of extra data attributes to response messages, particularly within the context of application man...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, supports the addition of custom data attributes to response messages and provides mechanisms for documenting these ...

</details>

---

#### GAP_0162: ATOM_066

**Requirement:** The system MAY include additional hyperlinks beyond specified requirements and MUST document these in ASPSP PSD2 documentation.

- **Strength:** `MAY`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** unknown
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports the inclusion of additional hyperlinks in API responses, particularly within the context of pagination for Org...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'I appreciate your question, but I need to clarify what you\'re asking about. Your prompt references "ASPSP PSD2 documentation" and requirements about "ad...

</details>

---

</details>

<details>
<summary><strong>Payment Initiation</strong> — 24 gap(s) | 10 not supported | 14 partial</summary>

### Payment Initiation

*24 gap(s) identified*

#### GAP_0001: ATOM_106

**Requirement:** The X-Request-ID header SHALL be mandatory for all payment retrieval requests and contain a unique UUID

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. x-fapi-interaction-id:
      in: "header"
      name: "x-fapi-interaction-id"
      required: false
      description: "An RFC4122 UID used as a correlation id."
      schema:
        type: "string"

...

2. obExternalAccountIdentification4Code:
      description: "Name of the identification scheme, in a coded form as published in an external list."
      type: "string"
      x-namespaced-enum:
        - ...

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

#### GAP_0010: ATOM_111

**Requirement:** The API SHALL return HTTP response code 204 when DELETE is sufficient for cancelling the payment

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0012: ATOM_098

**Requirement:** Payment status request SHALL include mandatory X-Request-ID header with UUID format

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. x-fapi-interaction-id:
      in: "header"
      name: "x-fapi-interaction-id"
      required: false
      description: "An RFC4122 UID used as a correlation id."
      schema:
        type: "string"

...

2. obExternalAccountIdentification4Code:
      description: "Name of the identification scheme, in a coded form as published in an external list."
      type: "string"
      x-namespaced-enum:
        - ...

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

#### GAP_0017: ATOM_024

**Requirement:** The API SHALL support payment cancellation through a two-step process: DELETE the resource and optionally start authorisation for cancellation

- **Strength:** `SHALL`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

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

#### GAP_0019: ATOM_058

**Requirement:** The system MUST transform payment initiation transaction status to 'CANC' (Cancelled) after successful cancellation and maintain this status while resource remains addressable.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

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

3. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'The WSO2 Financial Services Accelerator supports the cancellation of payment initiation transactions and the updating of their status t...

</details>

---

#### GAP_0020: ATOM_093

**Requirement:** Payment initiation transaction status MUST progress through defined states (RCVD, PATC, ACTC) during multilevel SCA process

- **Strength:** `MUST`
- **Section:** `f5ea71603fb5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0022: ATOM_114

**Requirement:** The API SHALL support GET /v1/{payment-service}/{payment-product}/{paymentId}/cancellation-authorisations for retrieving cancellation authorization sub-resources

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

2. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

3. ## Publish Open Banking APIs

!!! note
    WSO2 Open Banking Accelerator supports Accounts flow, Payments flow and Confirmation of Funds flow. Publish all three APIs before trying out the flows.

1. S...

</details>

---

#### GAP_0033: ATOM_109

**Requirement:** The API SHALL support DELETE /v1/{payment-service}/{payment-product}/{paymentId} endpoint for payment cancellation

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

2. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

3. ## Publish Open Banking APIs

!!! note
    WSO2 Open Banking Accelerator supports Accounts flow, Payments flow and Confirmation of Funds flow. Publish all three APIs before trying out the flows.

1. S...

</details>

---

#### GAP_0035: ATOM_104

**Requirement:** The API SHALL support GET /v1/{payment-service}/{payment-product}/{paymentId} endpoint for retrieving payment object content

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

2. obWritePaymentResponse5:
      type: "object"
      additionalProperties: false
      required:
        - "Data"
      properties:
        Data:
          type: "object"
          additionalProperties...

3. ## Publish Open Banking APIs

!!! note
    WSO2 Open Banking Accelerator supports Accounts flow, Payments flow and Confirmation of Funds flow. Publish all three APIs before trying out the flows.

1. S...

</details>

---

#### GAP_0042: ATOM_096

**Requirement:** Payment status retrieval SHALL support three payment service types: payments, bulk-payments, and periodic-payments

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

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

3. [wso2/financial-services-accelerator]
[{'type': 'text', 'text': 'This repository, `wso2/financial-services-accelerator`, supports payment status retrieval for `payments` through the `/payments/{paymen...

</details>

---

#### GAP_0044: ATOM_046

**Requirement:** Payment process must conclude with transaction status of either RJCT (Rejected) or ACSC (AcceptedSettlementCompleted).

- **Strength:** `MUST`
- **Section:** `d029f87e3d80`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0052: ATOM_097

**Requirement:** ASPSP SHALL validate that the payment-product parameter matches the payment product under which the paymentId was initiated

- **Strength:** `SHALL`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

2. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

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

#### GAP_0053: ATOM_205

**Requirement:** The scope parameter shall reference the resource in the format 'PIS:<paymentId>' for Payment Initiation Services

- **Strength:** `SHALL`
- **Section:** `13.1`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. openapi: "3.0.0"
info:
  title: "PaymentInitiationAPI"
  description: "Swagger for Payment Initiation API Specification"
  version: "v3.1"

servers:
  - url: "/open-banking/{version}/pisp"
paths:
  /p...

2. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

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

#### GAP_0055: ATOM_048

**Requirement:** The system MUST support payment initiation transaction status 'ACTC' (AcceptedTechnicalCorrect) when PSU authentication, syntactical and semantical product checks have been successful.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0057: ATOM_116

**Requirement:** The response body for HTTP code 202 SHALL include transactionStatus as mandatory field

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. x-fapi-interaction-id:
      in: "header"
      name: "x-fapi-interaction-id"
      required: false
      description: "An RFC4122 UID used as a correlation id."
      schema:
        type: "string"

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

#### GAP_0093: ATOM_050

**Requirement:** The system MUST support payment initiation transaction status 'ACCP' (AcceptedCustomerProfile) when financial risk profile including funds availability has been checked positively.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0107: ATOM_049

**Requirement:** The system MUST support payment initiation transaction status 'ACWC' (AcceptedWithChanges) when ASPSP applies changes to payment initiation parameters.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

</details>

---

#### GAP_0111: ATOM_077

**Requirement:** The ASPSP must validate confirmationCode in transaction authorization confirmation requests

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
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

#### GAP_0113: ATOM_110

**Requirement:** The ASPSP SHALL check that the payment-product matches the payment initiation addressed by paymentId

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0119: ATOM_112

**Requirement:** The API SHALL return HTTP response code 202 when DELETE requires PSU authorization for payment cancellation

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
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

#### GAP_0128: ATOM_054

**Requirement:** The system MUST support payment initiation transaction status 'PART' (PartiallyAccepted) for bulk payments when only some contained payments are processed successfully.

- **Strength:** `MUST`
- **Section:** `da818bb5b9ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0139: ATOM_105

**Requirement:** The payment-service path parameter SHALL accept values 'payments', 'bulk-payments', and 'periodic-payments'

- **Strength:** `SHALL`
- **Section:** `326a9719d7b5`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
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

#### GAP_0145: ATOM_103

**Requirement:** ASPSP MAY return XML payment status in pain.002 format for XML-encoded payment initiation requests

- **Strength:** `MAY`
- **Section:** `a4a84452c1ef`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

3. PSUOAuth2Security:
      type: "oauth2"
      description: "OAuth flow, it is required when the PSU needs to perform SCA with the ASPSP when a TPP wants to access an ASPSP resource owned by the PSU"
 ...

</details>

---

#### GAP_0157: ATOM_070

**Requirement:** TPPs MAY send an SCA status request to follow the SCA process during implicit authorization

- **Strength:** `MAY`
- **Section:** `648825991d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (4 sources)</summary>

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
<summary><strong>Security</strong> — 25 gap(s) | 10 not supported | 15 partial</summary>

### Security

*25 gap(s) identified*

#### GAP_0005: ATOM_195

**Requirement:** The Headers parameter must conditionally include psu-corporate-id if and only if PSU-Corporate-ID is included as a header of the HTTP-Request

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to have explicit support for conditionally including a `psu-corporate-id` header based on the presence ...

</details>

---

#### GAP_0013: ATOM_196

**Requirement:** The Headers parameter must conditionally include tpp-redirect-uri if and only if TPP-Redirect-URI is included as a header of the HTTP-Request

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0025: ATOM_199

**Requirement:** The TPP signature header shall use the keyId format 'SN=<serial_number>,CA=<certificate_authority>' for certificate identification

- **Strength:** `SHALL`
- **Section:** `4e52743eb3ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. #Details for Tsteing Purposes

SSA SoftwareId - oQ4KoaavpOuoE7rvQsZEOV
SSA Redirect Uri - https://www.google.com/redirects/redirect1


Sample Keystore information:
- Signing Kid = sCekNgSWIauQ34klRhDG...

2. #Details for Tsteing Purposes

SSA SoftwareId - 9ZzFFBxSLGEjPZogRAbvFd
SSA Redirect Uri - https://www.google.com/redirects/redirect1


Sample Keystore information:
- Signing Kid = BkHxeIHKyMKF6SgGwqYz...

3. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

</details>

---

#### GAP_0039: ATOM_202

**Requirement:** Header field names in the signing string shall be normalized to lowercase

- **Strength:** `SHALL`
- **Section:** `4e52743eb3ae`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to explicitly support or enforce the normalization of header field names to lowercase in the signing st...

2. [wso2/product-apim]
[{'type': 'text', 'text': "Based on the provided code snippets, there is no direct evidence or explicit implementation details that confirm the normalization of header field names ...

</details>

---

#### GAP_0072: ATOM_208

**Requirement:** The state parameter shall be a dynamical value set by the TPP to prevent XSRF attacks

- **Strength:** `SHALL`
- **Section:** `13.1`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

2. ## Inbuilt Gateway Enforcements

- [Dynamic Client Registration Request Policy](../learn/dcr-request-policy.md)
- [Dynamic Client Registration Response Policy](../learn/dcr-response-policy.md)
- [Cons...

3. ### Run tests

1. Use a tool and convert the private key (tpp.com.key) to a JWK. Use this JWK to update the value of the **keys** 
   array element in the JSON configuration.
2. Log in to the test sui...

</details>

---

#### GAP_0081: ATOM_178

**Requirement:** The Digest header field must be contained if and only if the Signature element is contained in the header of the request.

- **Strength:** `MUST`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

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

#### GAP_0098: ATOM_030

**Requirement:** The ASPSP SHALL tokenize card-account-id parameters such that actual card account numbers, IBANs, or PANs are not part of the API path definitions for data protection reasons

- **Strength:** `SHALL`
- **Section:** `b3c635de3d1c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. # API Security Open Banking allows API consumers to access financial data through open APIs, which requires greater API security. Therefore, open banking standards provide guidelines for security impl...

2. ### Authorization Request

WSO2 Open Banking Accelerator supports the following security features and fulfil FAPI requirements 
during Authorization flows:

  - OIDC Hybrid Flow
    - Request object v...

3. ### Resource Request

After an API consumer application obtains an access token, it is used to invoke a resource endpoint. In this request, 
the following validations will be performed:

- Token valid...

</details>

---

#### GAP_0100: ATOM_183

**Requirement:** When a TPP includes a signature as defined in signHTTP chapter 4, the TPP must include a Digest header as defined in RFC3230

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

2. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

3. ## DefaultTokenFilter 

Customize the following class to modify the token request, response, or error handling. 
``` java
com.wso2.openbanking.accelerator.identity.token.DefaultTokenFilter
```

!!! no...

</details>

---

#### GAP_0103: ATOM_184

**Requirement:** The Digest header must contain a hash of the message body, or if the message does not contain a body, the hash of an empty bytelist

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, appears to support hashing mechanisms, specifically SHA-256, for various security-related functions, including DPoP tok...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support Digest authentication, but it does not explicitly implement or verify the "Digest" header contai...

</details>

---

#### GAP_0106: ATOM_155

**Requirement:** The PSU-IP-Address header SHALL be contained if and only if the request was actively initiated by the PSU

- **Strength:** `SHALL`
- **Section:** `f4b3933a3ed2`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, does not appear to have explicit support for a "PSU-IP-Address" header or a mechanism to differentiate requests activel...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, does not directly support the automatic inclusion or exclusion of a `PSU-IP-Address` header based on whether a requ...

</details>

---

#### GAP_0108: ATOM_075

**Requirement:** The TPP must control session fixation using the state parameter in redirect SCA approach

- **Strength:** `MUST`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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

#### GAP_0110: ATOM_186

**Requirement:** A Signature header must be present when using signHTTP chapter 4

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

2. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

3. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

</details>

---

#### GAP_0116: ATOM_001

**Requirement:** The ASPSP SHALL use TLS version 1.2 or higher for all communication between TPP and ASPSP.

- **Strength:** `SHALL`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (6 sources)</summary>

1. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

2. which has authorised or registered an API consumer. The TSP revokes the certificate based on a verifiable and authentic revocation request. There are circumstances where the issuing CA needs to revoke...

3. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

</details>

---

#### GAP_0122: ATOM_189

**Requirement:** The Algorithm parameter in the Signature header is mandatory

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (5 sources)</summary>

1. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

2. ## Inbuilt Gateway Enforcements

- [Dynamic Client Registration Request Policy](../learn/dcr-request-policy.md)
- [Dynamic Client Registration Response Policy](../learn/dcr-response-policy.md)
- [Cons...

3. ## OBIdentityFilterValidator  
   
To perform validations at the filter level use the following class:

``` java
com.wso2.openbanking.accelerator.identity.token.validators.OBIdentityFilterValidator
``...

</details>

---

#### GAP_0132: ATOM_191

**Requirement:** The Algorithm parameter must identify SHA-256 or SHA-512 as the hash algorithm

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (3 sources)</summary>

1. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

2. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports SHA-256 and SHA-512 as hash algorithms for OAuth2 tokens and password hashing. The configuration for these alg...

3. [wso2/product-apim]
[{'type': 'text', 'text': '# Answer\n\nBased on the codebase context, the WSO2 API Manager repository **does support SHA-256 and SHA-512 hash algorithms**, but with important limit...

</details>

---

#### GAP_0135: ATOM_192

**Requirement:** The Headers parameter in the Signature header is mandatory

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

2. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

3. ## Inbuilt Gateway Enforcements

- [Dynamic Client Registration Request Policy](../learn/dcr-request-policy.md)
- [Dynamic Client Registration Response Policy](../learn/dcr-response-policy.md)
- [Cons...

</details>

---

#### GAP_0138: ATOM_193

**Requirement:** The Headers parameter must include digest and x-request-id

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

2. ## Configure Transport Layer Security (TLS) Parameters

1. Open the `<APIM_HOME>/repository/conf/deployment.toml` file.
2. Add the following configurations:

    ``` toml
    [transport.https.sslHostC...

3. # allowed_auth_url_parameters parameter is used to filter the Auth WebLink URL parameters.
allowed_auth_url_parameters = ["client_id", "scope", "response_type", "nonce", "redirect_uri", "binding_messa...

</details>

---

#### GAP_0140: ATOM_194

**Requirement:** The Headers parameter must conditionally include psu-id if and only if PSU-ID is included as a header of the HTTP-Request

- **Strength:** `MUST`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
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
[{'type': 'text', 'text': "I cannot find evidence in the provided codebase that this repository supports the requirement you're describing.\n\n## Analysis\n\nYou're asking whether th...

3. [wso2/product-apim]
[{'type': 'text', 'text': "I cannot find evidence in the codebase that this repository supports the requirement you're describing. <cite/>\n\n## Analysis\n\nBased on my search thro...

</details>

---

#### GAP_0142: ATOM_197

**Requirement:** No other entries beyond the specified mandatory and conditional headers may be included in the Headers parameter

- **Strength:** `MAY`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. #### Policy Attributes

| Attribute Name              | Display Name                                                        | Description                                                               ...

2. ## Inbuilt Gateway Enforcements

- [Dynamic Client Registration Request Policy](../learn/dcr-request-policy.md)
- [Dynamic Client Registration Response Policy](../learn/dcr-response-policy.md)
- [Cons...

3. # SMS service request headers can be defined as below.
[[open_banking.identity.ciba.auth_web_link.sms_notification.header]]
name = "Accept"
value = "application/json"
[[open_banking.identity.ciba.auth...

</details>

---

#### GAP_0144: ATOM_025

**Requirement:** TPPs SHOULD send PSU context data elements in all request messages within payment initiation or consent initiation transaction flows for enhanced risk management

- **Strength:** `SHOULD`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Initiate a consent

Please refer to the Step 1 and 2 in the [try-out-flow.md](..%2Fget-started%2Ftry-out-flow.md) for the more information on initiation of the consent.

2. ## Assumptions
- User's mobile number should be configured.
- Users will receive the notification as web links to authenticate and authorize the consent.
- For multiple users involved scenarios, Ident...

3. ## Multi auth user flows

For example of multi authorisation flow, we can think joint account scenario where all the users need to approve the consent. Below steps are mainly involved for multi auth u...

</details>

---

#### GAP_0146: ATOM_027

**Requirement:** TPP redirect URIs SHOULD comply with the domain secured by the eIDAS QWAC certificate in the CN or SubjectAltName fields

- **Strength:** `SHOULD`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. Certificate (QWAC) and Qualified Certificates for Electronic Seals (QSealC) to secure the transport layer and application layer with the API consumer. ####Qualified Web Authentication Certificate (QWA...

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

#### GAP_0149: ATOM_002

**Requirement:** The ASPSP SHALL follow NIST recommendations on cryptographical strength for cipher suite selections.

- **Strength:** `SHOULD`
- **Section:** `eef9ab97432c`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports NIST recommendations for cryptographic strength, particularly through its FIPS (Federal Information Processing...

2. [wso2/product-apim]
[{'type': 'text', 'text': "This repository, `wso2/product-apim`, appears to support NIST recommendations for cryptographic strength, specifically through its integration with FIPS ...

</details>

---

#### GAP_0152: ATOM_080

**Requirement:** ASPSPs and TPPs should follow OAuth2 Security Best Practice definitions as defined in OA-SecTop

- **Strength:** `SHOULD`
- **Section:** `508687390798`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### Authorization Request

WSO2 Open Banking Accelerator supports the following security features and fulfil FAPI requirements 
during Authorization flows:

  - OIDC Hybrid Flow
    - Request object v...

2. # API Security Open Banking allows API consumers to access financial data through open APIs, which requires greater API security. Therefore, open banking standards provide guidelines for security impl...

3. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

</details>

---

#### GAP_0153: ATOM_179

**Requirement:** A signature of the request by the TPP on application level might be mandated by ASPSP.

- **Strength:** `MAY`
- **Section:** `2bff2fd29855`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** partially_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (7 sources)</summary>

1. ### MTLS Enforcement Policy

MTLS Enforcement Policy is a policy designed to be engaged in the request flow of any request that requires MTLS to be mandatory. It will perform the below tasks.

- Manda...

2. ## Configure applications

The conformance suite has to run from the perspective of 2 clients. Therefore, two applications are required. Follow the
steps and create applications:

1. Create 2 applicat...

3. ### Resource Request

After an API consumer application obtains an access token, it is used to invoke a resource endpoint. In this request, 
the following validations will be performed:

- Token valid...

</details>

---

#### GAP_0158: ATOM_185

**Requirement:** The only hash algorithms that may be used to calculate the Digest are SHA-256 and SHA-512 as defined in RFC5843

- **Strength:** `MAY`
- **Section:** `ca341668f949`
- **Source:** `data\uploads\838576b0-1da9-498e-bcd3-b1f1d46287fc\Berlin Group.pdf`
- **Support Level:** not_supported
- **Confidence:** 100%

<details>
<summary>Supporting Evidence (2 sources)</summary>

1. [wso2/product-is]
[{'type': 'text', 'text': 'This repository, `wso2/product-is`, supports SHA-256 and SHA-512 as hash algorithms for various purposes, including password digests in user stores and OAu...

2. [wso2/product-apim]
[{'type': 'text', 'text': 'This repository, `wso2/product-apim`, appears to support Digest authentication, but the provided code snippets do not explicitly confirm that the Digest ...

</details>

---

</details>

## Critical Gaps Requiring Immediate Attention

The following requirements are **not supported** by the current WSO2 implementation:

| Gap ID | Requirement | Capability | Strength |
|--------|-------------|------------|----------|
| GAP_0014 | The system SHALL require X-Request-ID header as ma... | Authentication | SHALL |
| GAP_0016 | The TPP certificate content SHALL be compliant wit... | Certificate Management | SHALL |
| GAP_0017 | The API SHALL support payment cancellation through... | Payment Initiation | SHALL |
| GAP_0022 | The API SHALL support GET /v1/{payment-service}/{p... | Payment Initiation | SHALL |
| GAP_0025 | The TPP signature header shall use the keyId forma... | Security | SHALL |
| GAP_0032 | The system MUST provide SCA process status informa... | Authentication | MUST |
| GAP_0033 | The API SHALL support DELETE /v1/{payment-service}... | Payment Initiation | SHALL |
| GAP_0034 | The ASPSP SHALL provide a mandatory POST funds-con... | Funds Confirmation | SHALL |
| GAP_0039 | Header field names in the signing string shall be ... | Security | SHALL |
| GAP_0046 | ASPSP SHALL return ASPSP-SCA-Approach header with ... | Authentication | SHALL |
| GAP_0050 | The client_id parameter shall contain the organiza... | Authentication | SHALL |
| GAP_0051 | Account transaction requests MUST support bookingS... | Account Information | MUST |
| GAP_0052 | ASPSP SHALL validate that the payment-product para... | Payment Initiation | SHALL |
| GAP_0053 | The scope parameter shall reference the resource i... | Payment Initiation | SHALL |
| GAP_0056 | The system MUST provide hyperlinks with semantic t... | General | MUST |
| GAP_0057 | The response body for HTTP code 202 SHALL include ... | Payment Initiation | SHALL |
| GAP_0058 | The system SHALL support multi-currency accounts b... | Account Information | SHALL |
| GAP_0059 | The system SHALL return mandatory scaStatus and au... | Authentication | SHALL |
| GAP_0061 | Electronic signatures SHALL be included in HTTP he... | Authentication | SHALL |
| GAP_0062 | The system SHALL include ASPSP-SCA-Approach header... | Authentication | SHALL |
| GAP_0064 | Payment status response SHALL include fundsAvailab... | Funds Confirmation | SHALL |
| GAP_0066 | The system SHALL accept an optional withBalance qu... | Account Information | SHALL |
| GAP_0068 | The system SHALL support TPP-Redirect-URI header f... | Authentication | SHALL |
| GAP_0075 | The system SHALL update PSU identification data vi... | Authentication | SHALL |
| GAP_0078 | The system MUST support payment initiation transac... | Funds Confirmation | MUST |
| GAP_0080 | ASPSP SHALL provide list of available SCA methods ... | Authentication | SHALL |
| GAP_0081 | The Digest header field must be contained if and o... | Security | MUST |
| GAP_0083 | The system MUST support consent status 'terminated... | Consent Management | MUST |
| GAP_0086 | The API SHALL support signing of a group of transa... | Authentication | SHALL |
| GAP_0090 | The ASPSP SHALL provide a mandatory DELETE consent... | Consent Management | SHALL |
| GAP_0091 | In case of incorrect password, the TPP needs to as... | Authentication | MUST |
| GAP_0092 | The Read Transaction Details endpoint SHALL be acc... | Account Information | SHALL |
| GAP_0096 | The API SHALL support multiple level SCA where a t... | Authentication | SHALL |
| GAP_0097 | Error responses must use Content-Type application/... | Error Handling | MUST |
| GAP_0098 | The ASPSP SHALL tokenize card-account-id parameter... | Security | SHALL |
| GAP_0099 | Message parameters SHALL be encoded in spinal-case... | Data Access | SHALL |
| GAP_0100 | When a TPP includes a signature as defined in sign... | Security | MUST |
| GAP_0102 | The X-Request-ID header SHALL be mandatory and con... | Audit And Logging | SHALL |
| GAP_0103 | The Digest header must contain a hash of the messa... | Security | MUST |
| GAP_0107 | The system MUST support payment initiation transac... | Payment Initiation | MUST |
| GAP_0113 | The ASPSP SHALL check that the payment-product mat... | Payment Initiation | SHALL |
| GAP_0117 | The TPP-Redirect-URI header SHALL be mandatory for... | Authentication | SHALL |
| GAP_0123 | TPP MUST provide PSU credentials (User-ID and Pass... | Authentication | MUST |
| GAP_0125 | The Read Card Account List endpoint SHALL be acces... | Account Information | SHALL |
| GAP_0126 | Message parameters SHALL be encoded in Spinal-case... | Data Access | SHALL |
| GAP_0128 | The system MUST support payment initiation transac... | Payment Initiation | MUST |
| GAP_0133 | The Read Card Account Details endpoint SHALL be ac... | Account Information | SHALL |
| GAP_0135 | The Headers parameter in the Signature header is m... | Security | MUST |
| GAP_0137 | The TPP certificate SHALL indicate all roles the T... | Certificate Management | SHALL |
| GAP_0140 | The Headers parameter must conditionally include p... | Security | MUST |
| GAP_0145 | ASPSP MAY return XML payment status in pain.002 fo... | Payment Initiation | MAY |
| GAP_0146 | TPP redirect URIs SHOULD comply with the domain se... | Security | SHOULD |
| GAP_0148 | ASPSPs MAY offer a signing-baskets endpoint to sup... | Authentication | MAY |
| GAP_0151 | The system MAY provide optional 'fundsAvailable' b... | Funds Confirmation | MAY |
| GAP_0154 | It is recommended that the ASPSP inform the TPP ab... | Error Handling | SHOULD |
| GAP_0158 | The only hash algorithms that may be used to calcu... | Security | MAY |

## Recommendations

### High Priority
- Address **56** unsupported requirements through custom development or third-party solutions

### Medium Priority
- Review **101** partially supported requirements for configuration or extension opportunities

---

*Generated by Open Banking Compliance Agentic Workflow*
*Analysis powered by WSO2 Knowledge Base (217 requirements analyzed)*