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

*Note*: `X` represents the number of characters allocated in the record. The `9(5)v99` means this variable is a Numeric length of $8$ and $2$ digits after decimal. For example $3000000$ will be formatted to $30,000.00$

#### INPUTS

> `INFILE` - stands for **INPUT FILE**, given.

*Note*: File content has always interrelated records, and record (row) has always interrelated data.

> `REC-IN` - stands for **RECORD INPUT**

*Note*: Inside of record we have the following variables that we must declare because we need to initialize for inputs.

> `ACCNO-IN` - stands for **ACCOUNT NUMBER INPUT**,
for example (`001`, `002`, `003`).

> `ACCNAME-IN` - stands for **ACCOUNT NAME INPUT**, for example (MARK JEZEKIAH NAYRE, MARLON JAMES NAYRE, MARLON JAMES NAYRE).

> `TC` - stands for **TRANSCODE**, there are two only the `D` for **Deposit** and `W` for **Withdrawal**.

>`D` - stands for **Deposit**, add to current balance.

>`W` - stands for **Withdraw**, subtract to current balance.

> `AMOUNT` - the current input balance before the transaction takes place. It was given in the `INPUT FILE`.

### OUTPUTS

> `OUTFILE` - it is the expected output file after the process is finished.

> `OUTREC` -  temporary storage.

> `REC-OUT` - output of the record per each row, for example `(001  MARK JEZEKIAH NAYRE 45,000.00)`.

> `ACCNO-OUT` - The **ACCOUNT NUMBER OUTPUT**

> `ACCNAME-OUT` - The **ACCOUNT NAME OUTPUT**

> `BAL-OUT` - Balance output for each record after the transaction of the person was finished.

#### *Temporary, Accumulator, and with a constant value of string variables*

> `BAL` - Balance of account number of completer transaction happened. 

> `EOFSW` - flagging for the main process.

> `TACCNO` - TEMPORARY ACCOUNT NUMBER, the purpose of this is to break or to move on another record with a different `ACCOUNT NAME` 

> `TACCNAME` - TEMPORARY ACCOUNT NAME,

> `TOTDREC` - TEMPORARY DEPOSITOR RECORD

> `DCTR-OUT` - Total Deposit accumulated, it is the output written in the file.

> `DCTR` - collector it is equivalent to iteration variable.

> `TOTBREC ` - total balance record.

> `BCTR` - balance counter, iterative variable.

> `BCTR-OUT` - It will be written in the file `BALANCE COUNTER OUTPUT`.

### SUBPROCESS ROUTINE

> `MAIN-RTN` - main process.

> `INITIAL-RTN` - this is where input, output, accumulator, counter, and constant string are declared.

> `PROCESS-RTN` - Process routine whether deposit or withdraw - to add or subtract to the current balance.

> `ACCNT-BREAK-RTN` - value reset function.

> `FINISH-RTN` - to terminate the program.


#### *Note*: Ignore all the files except `README.md`, `index.html`, and `diagram.drawio`
