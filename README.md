## Reference
以下で紹介されているスクリプトの改変 (ダブルバイト環境でも実行できるよう追記 など)。
- [Create and configure your Edge profiles with PowerShell](https://danielpetri666.medium.com/create-new-custom-edge-profiles-with-powershell-e1ca47b53407) および [Improved PowerShell to create Edge Profiles](https://www.cloudappie.nl/improved-edge-profiles-powershell/)
- [Create new custom Edge profiles with PowerShell](https://danielpetri666.medium.com/create-new-custom-edge-profiles-with-powershell-e1ca47b53407) および [Create-EdgeProfile.ps1](https://github.com/danielpetri666/LazyAdmin/blob/main/Create-EdgeProfile.ps1)

## 注意事項
26 個以上のプロファイルを本スクリプトで作成しようとすると、Edge 自体の起動が起動できなくなる動作を確認。  
$array で指定する新しいプロファイルの数は 25 個までにする必要がある。  
なお、手動で作成する分にはその後何個でも可能 (確認した限りでは追加で 10 個、つまり 25 + 10 個までは作成できた)。  

## Sample
```
# Define an array
$array = @(
    "User01",
    "User02",
    "User03",
    "User04"
)

# Loop through each item in the array
foreach ($item in $array) {
    # Perform an action with each item
    Write-Output "Processing $item"
    New-EdgeProfile -Name $item
}
```
