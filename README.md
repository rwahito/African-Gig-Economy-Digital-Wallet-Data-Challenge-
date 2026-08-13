# African-Gig-Economy-Digital-Wallet-Data-Challenge-
As a data analyst, the aim of the project is to uncover the patterns and trends within the African gig economy. As well as identify any fraudulent activities through the analysis


## Measures
**1. TRANSACTIONS YOY % change**

Transaction YOY Change = <br>
VAR PreviousTransactions = <br>
    CALCULATE( <br>
        'Transaction History'[Total Amount Transacted], <br>
        DATEADD(Dates[full_date], -1, YEAR) <br>
    ) <br>

VAR CurrentTransactions = <br>
    [Total Amount Transacted] - PreviousTransactions <br>

VAR YoYChange = <br>
    DIVIDE( <br>
        CurrentTransactions - PreviousTransactions, <br>
        PreviousTransactions <br>
    ) <br>

RETURN <br>
      IF( <br>
            YoYChange > 0, <br>
            UNICHAR(129157) & " " & FORMAT(YoYChange, "+0.0%"), <br>
            IF( <br>
                YoYChange < 0, <br>
                UNICHAR(129158) & " " & FORMAT(ABS(YoYChange), "0.0%"), <br>
                "→ 0.0%" <br>
            ) <br>
        ) <br>
   
**2. FRAUD TRANSACTIONS YOY % CHANGE**
Fraud YoY Change = <br>

VAR PreviousFraud = <br>
    CALCULATE( <br>
          SUM('Transaction History'[fraud_loss_usd]), <br>
        'Transaction History'[is_fraud_flagged] = TRUE, <br>
        DATEADD(Dates[full_date],-1,YEAR) <br>
    ) <br>

VAR CurrentFraud = <br>
    PreviousFraud - 'Transaction History'[Fraudulent Transactions] <br>
    
VAR YoYChange = <br>
    DIVIDE( <br>
        CurrentFraud - PreviousFraud, <br>
        PreviousFraud <br>
    ) <br>

RETURN <br>
      IF( <br>
            YoYChange > 0, <br>
            UNICHAR(129157) & FORMAT(YoYChange, "+0.0%"), <br>
            IF( <br>
                YoYChange < 0, <br>
                UNICHAR(129158)  & FORMAT(ABS(YoYChange), "-0.0%"), <br>
                "→ 0.0%" <br>
            )
        )
