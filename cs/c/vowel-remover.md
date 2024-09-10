```c
#include <stdio.h>
#include <string.h>


char *shortcut (char *str_out, const char *str_in){
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

`\0` is the null terminator in C strings. It is a special character that marks
the end of a string. When you declare a string literal like "hello", C automatically
appends a null terminator at the end so it is stored as `{'h', 'e', 'l', 'l', 'o', '\0'}`.
It's purpose is to allow programs to know where a string ends without needing to
know its length in advance.
