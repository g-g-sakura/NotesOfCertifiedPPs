# Introduction
[JISEC-C0764](https://commoncriteriaportal.org/nfs/ccpfiles/files/ppfiles/c0764_epp.pdf) was developed by [National Institute of Advanced Industrial Science and Technology](https://www.cpsec.aist.go.jp/index_en.html), evaluated by [ECSEC Laboratory](https://www.ecsec.jp/publics/index/29/), an Evaluation Facility in Japan, and certified by [JISEC](https://www.ipa.go.jp/en/security/jisec/index.html), CC Certification Body in Japan.

The same company name as the evaluation facility is included as a contributor, which leads to concerns about impartiality.
This protection profile has several questionable descriptions as shown below:

## Section 5.1.2
### FDP_IFC.1/Import
A non-volatile memory of TOE is assigned as a *subject* of [FDP_IFC.1.1/Import](https://commoncriteriaportal.org/nfs/ccpfiles/files/ppfiles/c0764_epp.pdf#page=24).
Here the *subject* is considered as an active entity from the defintion of *subject* (see [3.88 of Common Criteria:2022 Part 1](https://commoncriteriaportal.org/files/ccfiles/CC2022PART1R1.pdf#page=25)).
Therefore the description can be considered as a non-conformity.

## Section 7.1
### FCS_COP.1/SKC
#### Table 7-1
##### AES-XTS
A cryptographic key length option 192-bit is specified for [AES-XTS](https://commoncriteriaportal.org/nfs/ccpfiles/files/ppfiles/c0764_epp.pdf#page=40).
AES-XTS using 192-bit is undefined as per [IEEE 1619](https://ieeexplore.ieee.org/document/8637988) and [NIST SP 800-38E](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-38e.pdf).
Therefore the description is considered as a non-conformity.

### [FCS_RBG_EXT.1](https://commoncriteriaportal.org/nfs/ccpfiles/files/ppfiles/c0764_epp.pdf#page=43)
It is stated that *<ins>italicized and underlined text</ins>* means "assignment completed".
Here FCS_RBG_EXT.1.2 is drafted using the style *<ins>italicized and underlined text</ins>*, but, the number of noise sources is unspecified.
Therefore, the assignment is not completed, and this contradicts with the style *<ins>italicized and underlined text</ins>*.

### FCS_COP.1/SigVer 
#### Table 7-3
##### ECDSA
[Three options](https://commoncriteriaportal.org/nfs/ccpfiles/files/ppfiles/c0764_epp.pdf#page=43) are specified for a cryptographic key length, 256-bit, 384-bit, and 512-bit.
Here, when using NIST P-521 curve, the cryptographic key length shall be 521-bit, as per [FIPS 186-5](https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.186-5.pdf#page=24).
Therefore the description is considered as a non-conformity.

##### [EdDSA](https://www.iso.org/obp/ui#iso:std:iso-iec:10118:-3:ed-4:v1:en#page=43)
[ISO/IEC 10118-3:2018 Clause 10](https://www.iso.org/obp/ui#iso:std:iso-iec:10118:-3:ed-4:v1:en) cannot be applied.  
Here EdDSA shall use either SHA-512 or SHAKE256 as per [FIPS 186-5](https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.186-5.pdf#page=28), while ISO/IEC [ISO/IEC 10118-3:2018 Clause 10](https://www.iso.org/obp/ui#iso:std:iso-iec:10118:-3:ed-4:v1:en) specifies the specification of SHA-256, which cannot be used with EdDSA.
Therefore the description is considered as a non-conformity.
