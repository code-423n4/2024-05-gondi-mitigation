# Gondi Mitigation Review details
- Total Prize Pool: $16,400 in USDC
  - HM awards: $13,140 in USDC
  - Judge awards: $1,460 in USDC
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Submit findings [using the C4 form](https://code4rena.com/contests/2024-05-gondi-mitigation-review/submit)
- Starts May 10, 2024 20:00 UTC)
- Ends May 20, 2024 20:00 UTC

## Important note 

Each warden must submit a mitigation review for *every* individual PR listed in the `Scope` section below. **Incomplete mitigation reviews will not be eligible for awards.**

## Findings being mitigated

Mitigations of all High and Medium issues will be considered in-scope and listed here.

### Highs
- [H-01: Merging tranches could make _loanTermination() accounting incorrect](https://github.com/code-423n4/2024-04-gondi-findings/issues/69)
- [H-02: Division before multiplication could lead to users losing 50% in WithdrawalQueue](https://github.com/code-423n4/2024-04-gondi-findings/issues/67)
- [H-03: Function distribute() lacks access control allowing anyone to spam and disrupt the pool's accounting](https://github.com/code-423n4/2024-04-gondi-findings/issues/64)
- [H-04: Function refinanceFromLoanExecutionData() does not check executionData.tokenId == loan.nftCollateralTokenId](https://github.com/code-423n4/2024-04-gondi-findings/issues/54)
- [H-05: triggerFee is stolen from other auctions during settleWithBuyout()](https://github.com/code-423n4/2024-04-gondi-findings/issues/50)
- [H-06: Function settleWithBuyout() does not call LoanManager.loanLiquidation() during a buyout](https://github.com/code-423n4/2024-04-gondi-findings/issues/49)
- [H-07: deployWithdrawalQueue() need clear _queueAccounting...](https://github.com/code-423n4/2024-04-gondi-findings/issues/48)
- [H-08: Incorrect circular array check in _updatePendingWithdrawalWithQueue flow , causing received funds added to the wrong queues](https://github.com/code-423n4/2024-04-gondi-findings/issues/47)
- [H-09: Incorrect accounting of _pendingWithdrawal in queueClaiming flow](https://github.com/code-423n4/2024-04-gondi-findings/issues/46)
- [H-10: The attackers front-running repayloans so that the debt cannot be repaid](https://github.com/code-423n4/2024-04-gondi-findings/issues/35)
- [H-11: Incorrect protocol fee implementation results in outstandingValues to be mis-accounted in Pool.sol](https://github.com/code-423n4/2024-04-gondi-findings/issues/33)
- [H-12: addNewTranche() no authorization from borrower](https://github.com/code-423n4/2024-04-gondi-findings/issues/29)
- [H-13: _processOffersFromExecutionData() lack of check executionData.duration<=offer.duration](https://github.com/code-423n4/2024-04-gondi-findings/issues/28)
- [H-14: mergeTranches()/refinancePartial() lack of nonReentrant](https://github.com/code-423n4/2024-04-gondi-findings/issues/27)
- [H-15: _baseLoanChecks() check errors for expire](https://github.com/code-423n4/2024-04-gondi-findings/issues/26)
- [H-16: validateOffer() reentry to manipulate exchangeRate](https://github.com/code-423n4/2024-04-gondi-findings/issues/24)
- [H-17: refinanceFull/addNewTranche reusing a lender's signature leads to unintended behavior](https://github.com/code-423n4/2024-04-gondi-findings/issues/13)

### Mediums
- [M-01: Invalid maxTranches check can result in maxTranche cap to be exceeded](https://github.com/code-423n4/2024-04-gondi-findings/issues/80)
- [M-02: A malicious user can take on a loan using an existing borrower's collateral in refinanceFromLoanExecutionData()](https://github.com/code-423n4/2024-04-gondi-findings/issues/76)
- [M-03: Function addNewTranche() should use protocolFee from Loan struct](https://github.com/code-423n4/2024-04-gondi-findings/issues/65)
- [M-04: Function Pool.validateOffer() does not work correctly in case principalAmount > currentBalance](https://github.com/code-423n4/2024-04-gondi-findings/issues/63)
- [M-05: Collected fees are never transferred out of Pool contract](https://github.com/code-423n4/2024-04-gondi-findings/issues/60)
- [M-06: Anyone can remove existing term without queueing through setTerms()](https://github.com/code-423n4/2024-04-gondi-findings/issues/59)
- [M-07: Attacker can front-run and pass in empty terms, making it impossible to confirmTerms()](https://github.com/code-423n4/2024-04-gondi-findings/issues/58)
- [M-08: Borrower signature could be reused in emitLoan()](https://github.com/code-423n4/2024-04-gondi-findings/issues/51)
- [M-09: Inconsistent accounting of undeployedAssets might result in undesired optimal range in the pool](https://github.com/code-423n4/2024-04-gondi-findings/issues/44)
- [M-10: Any liquidators can pretend to be a loan contract to validate offers, due to insufficient validation](https://github.com/code-423n4/2024-04-gondi-findings/issues/41)
- [M-11: AuctionLoanLiquidator#placeBid can be DoS](https://github.com/code-423n4/2024-04-gondi-findings/issues/37)
- [M-12: Pool.getMinTimeBetweenWithdrawalQueues current calculations may not be sufficient](https://github.com/code-423n4/2024-04-gondi-findings/issues/23)
- [M-13: confirmBaseInterestAllocator() change BaseInterestAllocator may pay large getReallocationBonus](https://github.com/code-423n4/2024-04-gondi-findings/issues/22)
- [M-14: loanLiquidation() calculation of interest is not accurate](https://github.com/code-423n4/2024-04-gondi-findings/issues/20)
- [M-15: confirmUnderwriter() need to recalculate getMinTimeBetweenWithdrawalQueues](https://github.com/code-423n4/2024-04-gondi-findings/issues/17)
- [M-16: distribute() Use the wrong end time to break maxSeniorRepayment's expectations](https://github.com/code-423n4/2024-04-gondi-findings/issues/16)
- [M-17: loan.hash() does not contain protocolFee](https://github.com/code-423n4/2024-04-gondi-findings/issues/15)
- [M-18: distribute() when can't repay all lenders, may lack of notification to LoanManager for accounting](https://github.com/code-423n4/2024-04-gondi-findings/issues/10)
- [M-19: Bidders might lose funds due to possible racing condition between settleWithBuyout and placeBid](https://github.com/code-423n4/2024-04-gondi-findings/issues/6)
- [M-20: Hardcoded incorrect getLidoData timestamp, resulting in incorrect base point Apr. Loans can be validated with a substantially low baseRate interest](https://github.com/code-423n4/2024-04-gondi-findings/issues/3)


[ ⭐️ SPONSORS ADD INFO HERE ]

## Overview of changes

Please provide context about the mitigations that were applied if applicable and identify any areas of specific concern.

## Scope

### Branch
[ ⭐️ SPONSORS ADD A LINK TO THE BRANCH IN YOUR REPO CONTAINING ALL PRS ]

### Mitigation of High & Medium Severity Issues
[ ⭐️ SPONSORS ADD ALL RELEVANT PRs TO THE TABLE BELOW:]

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo. 

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| https://github.com/pixeldaogg/florida-contracts/tree/fix/69 | H-01 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/67 | H-02 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/64 | H-03 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/54 | H-04 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/50 | H-05 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/49 | H-06 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/48 | H-07 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/47 | H-08 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/46 | H-09 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/35 | H-10 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/33 | H-11 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/29 | H-12 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/28 | H-13 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/27 | H-14 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/26 | H-15 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/24 | H-16 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/13 | H-17 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/80 | M-01 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/76 | M-02 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/65 | M-03 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/63 | M-04 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/60 | M-05 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/59 | M-06 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/58 | M-07 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/51 | M-08 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/44 | M-09 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/41 | M-10 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/37 | M-11 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/23 | M-12 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/22 | M-13 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/20 | M-14 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/17 | M-15 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/16 | M-16 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/15 | M-17 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/10 | M-18 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/6 | M-19 | This mitigation does XYZ | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/3 | M-20 | This mitigation does XYZ | 


## Out of Scope

Please list any High and Medium issues that were judged as valid but you have chosen not to fix.
