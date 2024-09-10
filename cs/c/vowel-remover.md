```c
#include <stdio.h>
#include <string.h>


char *shortcut (char *str_out, const char *str_in)
{
  char *vowel = "aeoui";
  int j=0;
  for(int i=0;i<strlen(str_in);i++){
    if(strchr(vowel,str_in[i]) == 0){
    	str_out[j] = str_in[i];
    	j++;
	}
  }
  str_out[j] = '\0';
  return str_out;
}
```
