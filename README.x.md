cat.|instr.|output
-|-|-
```scaffold.chain(xchain)```|*```starport scaffold chain github.com/deep2essence/xchain --no-module```*|*```app/,cmd,/docs/,testutil/,vue/,config.yml```<br><br>```go.mod,go.sum,readme.md,.github/,.gitignore```*
```scaffold.module(loan)```|*```starport scaffold module loan --dep bank```*|*generated:```proto/loan/,x/loan/,testutil/keeper/loan.go```<br>modified:```app/app.go,docs/static/openapi.yml```*
```scaffold.list(loan)```|*```starport scaffold list loan amount fee collateral deadline state borrower lender --no-message```*|***query+types+genesis**<br>generated: ```proto/loan/loan.proto```,<br>```x/loan/client/cli/query_loan*.go,```,<br>```x/loan/types/,```,<br>```x/loan/keeper/*loan*.go```<br><br>modified:**```proto/loan/query.proto+genesis.proto```**<br>```x/loan/types+```*
```scaffold.message(request-loan)```|```starport scaffold message request-loan amount fee collateral deadline```|***tx+message+codec+handler**<br>modified:```tx.proto```*
