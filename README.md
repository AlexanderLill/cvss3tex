# cvss3tex
Latex Implementation for CVSSv3


## Info

This LaTeX-Script calculates the CVSSv3 Base Score (see [https://www.first.org/cvss/specification-document]) given the necessary 8 parameters in the following format:
* (AV) Attack Vector:
    *  (N)etwork
    *  (A)djacent
    *  (L)ocal
    *  (P)hysical
* (AC) Attack Complexity:
    *  (L)ow
    *  (H)igh
* (PR) Privileges Required
    *  (N)one
    *  (L)ow
    *  (H)igh
* (UI) User Interaction
    * (N)one
    * (R)equired
* (S) Scope
    * (U)nchanged
    * (C)hanged
* (C) Confidentiality Impact
    * (H)igh
    * (L)ow
    * (N)one
* (I) Integrity Impact
    * (H)igh
    * (L)ow
    * (N)one
* (A) Availability Impact
    * (H)igh
    * (L)ow
    * (N)one

## Usage

You can use `\cvssBaseScore{AV}{AC}{PR}{UI}{S}{C}{I}{A}` and `\cvssBaseScorePretty{AV}{AC}{PR}{UI}{S}{C}{I}{A}` to calculate the CVSSv3 Base Score either without or with the given parameters. The possible values for the parameters are shown in the "Info" section.


## Examples

```
\cvssBaseScorePretty{N}{L}{N}{N}{U}{L}{L}{L}
\cvssBaseScorePretty{N}{L}{N}{N}{C}{L}{L}{L}
\cvssBaseScore{N}{L}{N}{N}{C}{L}{L}{L}
```

Output:
```
AV: N AC: L PR: N UI: N S: U C: L I: L A: L  Score: 7.3
AV: N AC: L PR: N UI: N S: C C: L I: L A: L  Score: 8.3
8.3
```


## Testing

The formulas and the parsing can be tested by executing the command `\cvssTest`


## Licensing

This code is licensed under the GNU General Public License v3.0 [http://www.gnu.org/licenses/gpl-3.0.en.html]
