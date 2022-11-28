# Description
 
The PKI Consortium is managing a PQC Capabilities Matrix (PQCCM) of software applications, libraries and hardware that includes support for 
Post Quantum Cryptography, without endorsing their implementation or quality.

The list includes a wide variety of software applications, libraries, and hardware from different vendors. 
The list should be considered a living document and a starting point. Considering the rapid change in the area such things can vary from day to day and complete freshness of information can only be gathered from vendors directly. 

The PKI Consortium is actively working to promote the adoption of Post-Quantum Cryptography, and the capabilities matrix is a key part of that effort.

What the PQCCM do:
* collect and aggregate information on PQC capabilities across the cybersecurity landspace (vendors, software, hardware, etc..)

What the PQCCM doesn't do:
* review, vet, verify or test implementations or interoperability
* source code review, formal review of algorithms, etc.
* provide information, documentation or any recommended usage of Post Quantum Cryptography

No other activity besides what is listed under PQCCM DOs is under the purview of PKI Consortium (unless explicitly stated otherwise)".




# Capabilities

The table lists information from vendors related to support for Post Quantum Cryptography.
| Vendor|Product     |Type|Last updated|X.509 Certs|Composite Certs|Hybrid Certs|HSS/LMS         |XMSS              |Falcon|Dilithium         |SPHINCS+|Kyber             |BIKE|McEliece|HQC|Other|
|:------|:-----------|:---|:---------|:----------|:--------------|:-----------|:-----------------|:-----------------|:-----|:-----------------|:-------|:-----------------|:---|:-------|:--|:---|
|[Securosys](#securosys)|Primus|HSM |2022-11-28|:x:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x: |:x:     |:x:|:x:|
|[Utimaco](#utimaco)|CryptoServer|HSM |2022-11-28|:x:        |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x: |:x:     |:x:|:x:|
|[Thales](#thales)|Luna|HSM |2022-11-22|:x:        |:x:            |:x:        |:heavy_check_mark:|:heavy_check_mark:|:x:   |:heavy_check_mark:|:x:     |:heavy_check_mark:|:x: |:x:     |:x:|:x:|
|[Entrust](#entrust)|nShield|HSM |2022-11-22|:x:        |:x:            |:x:        |:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x: |:x:     |:x:|:heavy_check_mark:|
|[Entrust](#entrust)|PKIaaS|PKI Software |2022-11-22|:heavy_check_mark:|:heavy_check_mark:|:x:        |:x:|:x:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:x:|:x: |:x:     |:x:|:x:|
|[Bouncy Castle](#bouncy-castle)|BC|API |2022-11-22|:heavy_check_mark:|:heavy_check_mark:|:x:        |:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|:heavy_check_mark:|
|[Keyfactor](#keyfactor)|SignServer|Signing Software|2022-11-22|:x:        |:x:            |:x:        |:x:|:x:|:x:   |:x:|:heavy_check_mark:     |:x:|:x: |:x:     |:x:|:x:|
|[Keyfactor](#keyfactor)|EJBCA|PKI Software|2022-11-22|:heavy_check_mark:        |:x:            |:x:        |:x:|:x:|:heavy_check_mark:|:x:|:x:     |:x:|:x: |:x:     |:x:|:x:|

The following table contains references
|Algorithm|Reference|Last updated|
|:------|:-----------|:---|
|Composite keys and certificates|https://datatracker.ietf.org/doc/draft-ounsworth-pq-composite-keys/|2022-11-28|
|HSS/LMS|https://www.rfc-editor.org/rfc/rfc8708.html|2022-11-28|


## Securosys
Primus HSM (https://www.securosys.com/en/products/primus-hardware-security-modules-hsm) manufactured by https://www.securosys.com/en/. The listed features are based on the roadmap for 2023 and are subject to change depending on market demand and industry research.

## Utimaco

uTrust Identiy and QSafe firmware extension. Software simulator availabe, Dilithium in process of updated to round 3 version

## Thales

Functional module for Luna. Need functional modules enabled.

## Bouncy Castle
Java and C# APIs with all NIST candidate support, and some older ones. [Available as open source software](https://www.bouncycastle.org/). All NIST candidated available in Java from version 1.72 and C# from version 2.0.0.

The [Bouncy Castle for kotlin](https://github.com/bcgit/bc-kotlin) open source package provides a script/command line interface for generating certificate chains with different algorithms. 

## Entrust 
nShield

The Entrust nShield Post-Quantum SDK enables post-quantum cryptographic applications for nShield HSMs with the CodeSafe SDK.
https://www.entrust.com/-/media/documentation/datasheets/entrust-pqc-option-pack-ds.pdf

PKIaaS

The Entrust PKI as a Service (PKIaaS) for Post-Quantum Beta Program supports all three algorithms selected in round 3 of the NIST competition and can provide composite and pure quantum CA hierarchies.
https://www.entrust.com/digital-security/certificate-solutions/products/pki/managed-services/pki-as-a-service

## Keyfactor
SignServer

SignServer performs server side signing and is capable of Post-Quantum signatures on CMS (RFC5662) messages. Available as open source software from [SignServer Community v5.9.1](https://doc.primekey.com/signserver/signserver-release-information/signserver-release-notes/signserver-community-5-9-1-release-notes).

EJBCA

EJBCA PKI software can issue X.509 certificates supporting Post-Quantum algorithms. Available for private test.

# Links
[Composite keys and signatures](https://datatracker.ietf.org/doc/draft-ounsworth-pq-composite-keys/)

[Hybrid multiple algorithm certificates](https://datatracker.ietf.org/doc/draft-truskovsky-lamps-pq-hybrid-x509/)

NIST Recommendation for Stateful Hash-Based Signature Schemes [SP800-208](https://csrc.nist.gov/publications/detail/sp/800-208/final)
