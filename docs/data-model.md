# Data Model

The project utilizes a single-table analytical model imported from a static data source.

## Semantic Model Structure
- **Type**: Single-table analytical model.
- **Table Name**: `UPI Transactions`

## Important Columns
- `TransactionID` (String)
- `TransactionDate` (Date)
- `TransactionTime` (Time)
- `Amount` (Decimal)
- `RemainingBalance` (Decimal)
- `BankNameSent` (String)
- `BankNameReceived` (String)
- `City` (String)
- `Gender` (String)
- `TransactionType` (String)
- `Status` (String)
- `DeviceType` (String)
- `PaymentMethod` (String)
- `PaymentMode` (String)
- `MerchantName` (String)
- `Purpose` (String)
- `CustomerAge` (Integer)
- `Currency` (String)

## Calculated Columns
- `Age Groups`: Categorizes customers based on age.
  - Formula: `IF('UPI Transactions'[CustomerAge]<=25,"A1", IF('UPI Transactions'[CustomerAge]<=35,"A2","A3"))`

## Measures
No explicit DAX measures are defined in the model. The dashboard relies on Power BI's implicit measures (like Sum, Average, Count) on columns such as `Amount` and `RemainingBalance`.

## Relationships
As this is a single-table model, there are no complex relationships or a star schema defined. All dimensional filtering is applied directly to the `UPI Transactions` table.
