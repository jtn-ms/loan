### Build
cat.|instr.|output
-|-|-
```scaffold.chain(xchain)```|*```starport scaffold chain github.com/deep2essence/xchain --no-module```*|*```app/,cmd,/docs/,testutil/,vue/,config.yml```<br><br>```go.mod,go.sum,readme.md,.github/,.gitignore```*
```scaffold.module(loan)```|*```starport scaffold module loan --dep bank```*|*generated:```proto/loan/,x/loan/,testutil/keeper/loan.go```<br>modified:```app/app.go,docs/static/openapi.yml```*
```scaffold.list(loan)```|*```starport scaffold list loan amount fee collateral deadline state borrower lender --no-message```*|***query+types+genesis**<br>generated: ```proto/loan/loan.proto```,<br>```x/loan/client/cli/query_loan*.go,```,<br>```x/loan/types/,```,<br>```x/loan/keeper/*loan*.go```<br><br>modified:**```proto/loan/query.proto+genesis.proto```**<br>```x/loan/types+```*
```scaffold.message(request-loan)```|```starport scaffold message request-loan amount fee collateral deadline```|***tx+message+codec+handler**<br>modified:```tx.proto```*
```implement.request```|*fillin:```keeper.RequestLoan```<br>```types.BankKeeper.SendCoinsFromAccountToModule```<br>```MsgRequestLoan.ValidateBasic```*
```scaffold.message(approve.loan)```|```starport scaffold message approve-loan id:uint```|***tx+message+codec+handler**<br>modified:```tx.proto```*
```implement.approve```|*fillin:```keeper.ApproveLoan```<br>```errors.ErrWrongLoanState```<br>```types.BankKeeper.SendCoin```*
```scaffold.message(repay.loan)```|```starport scaffold message approve-loan id:uint```|***tx+message+codec+handler**<br>modified:```tx.proto```*
```scaffold.message(liquidate.loan)```|```starport scaffold message liquidate-loan id:uint```|***tx+message+codec+handler**<br>modified:```tx.proto```*


### Test
cat.|command
-|-
```start.chain```|```starport chain serve```
```request.loan```|```loand tx loan request-loan 100token 2token 200token 500 --from alice ```
```query.loan```|```loand query loan list-loan```

### Question
q|a
-|-
*```SendCoinsFromAccountToModule```only interface added, how can it works?*|

