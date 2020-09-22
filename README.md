<div align="center">

## Using C\+\+ for CGI work\.


</div>

### Description

This isn't much, but it shows you how to use C++ to make CGI programs. NOTE: Please read "Explanations/Assumptions" for instructions on how to use this.
 
### More Info
 
Compile this code, and start up PWS(Personal Web Server), set the directory permissions to read and execute, put the exe in the directory, then type: <BR>

http://localhost/nameofexe.exe <BR>

I will add more code later, but I don't have enough time right now...

If the code is successful, it should output "GET" minus the quotes.


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Dennis Wrenn](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dennis-wrenn.md)
**Level**          |Beginner
**User Rating**    |3.5 (14 globes from 4 users)
**Compatibility**  |C, C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__3-9.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dennis-wrenn-using-c-for-cgi-work__3-1030/archive/master.zip)





### Source Code

```
#include <cstdio>
#include <string>
int main()
{
	using namespace std;
	char * pcReqMtd;
	fprintf(stdout, "Content-type: text/html\n\n");
	pcReqMtd = getenv("REQUEST_METHOD");
	fprintf(stdout, pcReqMtd);
	return 0;
}
```

