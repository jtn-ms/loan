cat.|instr.|output
-|-|-
```scaffold.chain(xchain)```|*```starport scaffold chain github.com/deep2essence/xchain --no-module```*|*```app/,cmd,/docs/,testutil/,vue/,config.yml```<br><br>```go.mod,go.sum,readme.md,.github/,.gitignore```*
```scaffold.module(loan)```|*```starport scaffold module loan --dep bank```*|*generated:```proto/loan/,x/loan/,testutil/keeper/loan.go```<br>modified:```app/app.go,docs/static/openapi.yml```*
```scaffold.list(loan)```|*```starport scaffold list loan amount fee collateral deadline state borrower lender --no-message```*|