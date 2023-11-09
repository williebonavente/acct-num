# Basic Banking System Flowcharting - Structure Flowchart

## Given: A file of transactions `INFILE`

### Input Record

#### `INFILE`

|`ACCNO`|`ACCNAME`|`TRANSCODE`|`AMOUNT`|
|-----|---|---|---|
|`X(3)`|`X(24)`|`(TC)X`|`9(5)V99`|
|`001`| MARK JEZEKIAH NAYRE | `D`| $3000000$|
|`001`| MARK JEZEKIAH NAYRE | `W`| $0500000$|
|`001`| MARK JEZEKIAH NAYRE | `D`| $2000000$|
|`002`| RAINAH CASSANDRA NAYRE | `D`| $50000000$|
|`002`| RAINAH CASSANDRA NAYRE | `W`| $1000000$|
|`003`| MARLON JAMES NAYRE | `D`| $3000000$|

## Requirements: `OUTFILE`

**WRITE** `ACCNO`, `ACCNAME`, and `BALANCE`. At end of File, **WRITE** the total depositors and the total accumulated balances.

*Note:* Records are arranged according to `ACCNO`.

## `OUTFILE`: Output Layout

```
                        MJRC SAVING BANK
                    Maypajo, Caloocan Branch
                        DEPOSITOR’S REPORT

    ACCOUNT			     ACCOUNT			     BALANCE
     NUMBER				  NAME				     AMOUNT

      001			MARK JEZEKIAH NAYRE      	45,000.00
      002			RAINAH CASSANDRA NAYRE		40,000.00
      003			MARLON JAMES NAYRE			30,000.00

TOTAL DEPOSITORS: 3 
TOTAL ACCUMULATED BALANCES: 115,000.00 

TOTAL ACCUMULATED BALANCES: 115,000.00 
```

### Variable Documentation Proper

*Note*: `X` stands for the number of characters allocated in the record. The `9(5)v99` means this variable is Numeric type of length $8$ and $2$ digits after decimal. For example: $30,000.00$ it is int the *COBOL* legacy system.

#### INPUTS

> `INFILE` - stands for **INPUT FILE**, given.

*Note*: File content have always interrelated records, and record (row) have always interrelated data.

> `REC-IN` - stands for **RECORD INPUT**

*Note*: Inside of record we have the following variables that we must declare, because we need to initialize for inputs.

> `ACCNO-IN` - stands for **ACCOUNT NUMBER INPUT**,
for example (`001`, `002`, `003`).

> `ACCNAME-IN` - stands for **ACCOUNT NAME INPUT**, for example (MARK JEZEKIAH NAYRE, MARLON JAMES NAYRE, MARLON JAMES NAYRE).

> `TC` - stands for **TRANSCODE**, there are two only the `D` for **Deposit** and `W` for **Withdrawal**.

>`D` - stands for **Deposit**, add to current balance.

>`W` - stands for **Withdraw**, subtract to current balance.

> `AMOUNT` - the current input balance before the transaction takes place. It was given in the `INPUT FILE`.

### OUTPUTS

> `OUTFILE` - it is the expected output file after the process was finished.

> `OUTREC` - output of the record per each row, for example `(001				MARK JEZEKIAH NAYRE      		45,000.00)`

> `REC-OUT`

> `ACCNO-OUT` - The **ACCOUNT NUMBER OUTPUT**

> `ACCNAME-OUT` - The **ACCOUNT NAME OUTPUT**

> `BAL-OUT` - Balance output for each record after the transaction of the person was finished.

#### *Temporary, Accumulator, and with constant value of string variables*

> `BAL`

> `EOFSW`

> `TACCNO`

> `TACCNAME`

> `TOTDREC`

> `DCTR`

> `DCTR-OUT`

> `DCTR`

> `TOTBREC `

> `BCTR`

> `BCTR-OUT`

### SUBPROCESS ROUTINE

> `MAIN-RTN`

> `INITIAL-RTN`

> `PROCESS-RTN`

> `ACCNT-BREAK-RTN`

> `FINISH-RTN`

### Behind Logical Reasoning

### Tracing


### Frequently Asked Questions


#### *Note*: Ignore all the files except `README.md` and `diagram.drawio`