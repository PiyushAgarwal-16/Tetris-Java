if (-not (Test-Path bin)) { mkdir bin } ; javac -d bin (Get-ChildItem -Recurse -Filter *.java).FullName ; if ($?) { java -cp "bin;res" main.Main }

For linux:
mkdir -p bin && javac -d bin $(find . -name "*.java") && java -cp "bin:res" main.Main 
