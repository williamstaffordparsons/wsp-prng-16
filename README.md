# WSP-PRNG-16
© 2024 William Stafford Parsons

## About
WSP-PRNG-16 is a 16-bit pseudorandom number generator algorithm as a substantial improvement to standard library `rand()` functions, PCG16 and Xorshift16 "798".

Read more [here](https://williamstaffordparsons.github.io/wsp-prng-16/).

## Example
``` c
#include <stdio.h>
#include "wsp_prng_16.h"

int main(void) {
  struct wsp_prng_16_s s = {
    .increment = 0,
    .increment_offset = 0
  };
  unsigned char i = 0;

  while (i != 10) {
    i++;
    printf("Result %u is %u.\n", i, wsp_prng_16_randomize(&s));
  }

  return 0;
}
```
