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
- [M-01: Title](link to Github issue)
- [M-02: Title](link to Github issue)
- [M-03: Title](link to Github issue)
- [M-04: Title](link to Github issue)
- [M-05: Title](link to Github issue)
- [M-06: Title](link to Github issue)
- [M-07: Title](link to Github issue)
- [M-08: Title](link to Github issue)
- [M-09: Title](link to Github issue)
- [M-10: Title](link to Github issue)
- [M-11: Title](link to Github issue)
- [M-12: Title](link to Github issue)
- [M-13: Title](link to Github issue)
- [M-14: Title](link to Github issue)
- [M-15: Title](link to Github issue)
- [M-16: Title](link to Github issue)
- [M-17: Title](link to Github issue)
- [M-18: Title](link to Github issue)
- [M-19: Title](link to Github issue)
- [M-20: Title](link to Github issue)


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
| https://github.com/your-repo/sample-contracts/pull/XXX | H-01 | This mitigation does XYZ | 

## Out of Scope

Please list any High and Medium issues that were judged as valid but you have chosen not to fix.
