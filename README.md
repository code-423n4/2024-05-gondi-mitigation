# Gondi Mitigation Review details
- Total Prize Pool: $16,400 in USDC
  - HM awards: $13,140 in USDC
  - Judge awards: $1,460 in USDC
- [Warden guidelines for C4 mitigation reviews](https://code4rena.notion.site/Guidelines-for-C4-mitigation-reviews-ed10fc5cfbf640bd8dcec66f38b343c4)
- Submit findings [using the C4 form](https://code4rena.com/contests/2024-05-gondi-mitigation-review/submit)
- Starts May 14, 2024 20:00 UTC
- Ends May 24, 2024 20:00 UTC

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



## Overview of changes

All invidivual fixes are addressed in a separate PR. The branche feature/developWithOpt contains the merge of all such features + a few that were found by other auditors. Because of contract size issues when adding all fixes, the following has changed:
 - There's no bonus on Pool reallocation (we expect the dao to run this function and incur the cost)
 - In refinancePartial, we don't allow extra principal (this is a corner case and can still be done with addNewTranche)
 - Some of the two step variable changes in the Pool (LoanManager) have been moved to a helper contract.
Feel free to ignore issues regarding the PoolOfferHandler since we are working on a different one given the limitations of the existing one.
 - Please note the out-of-scope item H-10. While not in scope for awards, general commentary on its design is welcome.

## Scope

### Branch
https://github.com/pixeldaogg/florida-contracts/pull/394

### Mitigation of High & Medium Severity Issues

Wherever possible, mitigations should be provided in separate pull requests, one per issue. If that is not possible (e.g. because several audit findings stem from the same core problem), then please link the PR to all relevant issues in your findings repo. 

| URL | Mitigation of | Purpose | 
| ----------- | ------------- | ----------- |
| https://github.com/pixeldaogg/florida-contracts/tree/fix/69 | H-01 | Only tranche lender can call `mergeTranches` so it assumes the responsibility. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/67 | H-02 | Change order in multiplication/division as suggested.| | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/64 | H-03 | Added caller check to avoid anyone calling `distribute`. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/54 | H-04 | Added tokenIdCheck | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/50 | H-05 | Change to `safeTransferFrom` buyer  | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/49 | H-06 | Added loanLiquidation call | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/48 | H-07 | Clear state vars | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/47 | H-08 | Need to break 1 before. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/46 | H-09 | Missing `+` | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/33 | H-11 | Passing protocol fee| 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/29 | H-12 | Added caller check | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/28 | H-13 | Added duration check. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/27 | H-14 | Added nonReentrant. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/26 | H-15 | Strict -> `<=` | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/24 | H-16 | validateOffer changed to view so validators cannot change state.| 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/13 | H-17 | Check trancheIndex to differentiate between refiFull / addNewTranche | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/80 | M-01 | Check total tranches + min amount per tranche. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/76 | M-02 | Checking signature from the existing borrower. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/65 | M-03 | addNewTranche uses protocolFee from struct. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/63 | M-04 | changed to reallocate(currentBalance, principalAmount, true) instead of proposed solution (same result) to be compliant with the interface | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/60 | M-05 | Added collectFees method | 
| https://github.com/pixeldaogg/florida-contracts/pull/367 | M-06, M-07 | Terms must be passed in the confirm as well. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/51 | M-08 | Only adding a comment here. Borrower should always set block.timestamp +small time delta as expiration to control when the loan can be started.| 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/44 | M-09 | Missing collected fees in accounting | 
| https://github.com/pixeldaogg/florida-contracts/pull/397 | M-10 | Check loanContract | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/37 | M-11 | There's a min bid now. This + the min improvement invalidates DoS. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/23 | M-12 | Limit auction extensions. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/22 | M-13 | Proactively reallocate (we got rid of the bonus though) | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/20 | M-14 | Corrected calculation of fees as suggested. | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/17 | M-15 | Added check (maxDuration cannot be longer.) | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/16 | M-16 | Changed to loan end time (instead of current timestamp) | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/15 | M-17 | Added field in hash | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/10 | M-18 | Always call loanManager (even if 0 proceeds) | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/6 | M-19 | Strict to `>=` | 
| https://github.com/pixeldaogg/florida-contracts/tree/fix/3 | M-20 | Set right value for getLidoData timestamp | 


## Out of Scope

H-10 - Refinacing a loan locks the loan. Adding a tranche can only be accepted by the borrower now (H-10). External actors can only front-run a limited number of times.
