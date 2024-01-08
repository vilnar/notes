## mono
csc hello.cs
mono hello.exe

csc hellowinform.cs -r:System.Windows.Forms.dll


msbuild myproject.csproj
"c:\Program Files\Mono\bin\msbuild" MobileHotspot\MobileHotspot.csproj -p:Configuration=Release
