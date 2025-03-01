## Reference
以下で紹介されているスクリプトの改変 (ダブルバイト環境でも実行できるよう追記 など)。
- [Create and configure your Edge profiles with PowerShell](https://danielpetri666.medium.com/create-new-custom-edge-profiles-with-powershell-e1ca47b53407) および [Improved PowerShell to create Edge Profiles](https://www.cloudappie.nl/improved-edge-profiles-powershell/)
- [Create new custom Edge profiles with PowerShell](https://danielpetri666.medium.com/create-new-custom-edge-profiles-with-powershell-e1ca47b53407) および [Create-EdgeProfile.ps1](https://github.com/danielpetri666/LazyAdmin/blob/main/Create-EdgeProfile.ps1)

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
