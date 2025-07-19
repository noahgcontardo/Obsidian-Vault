23 24 3c 83 84 ba bb

need to narrow down bad chars. One may immediately be suspicious that "23, 3c, 83, ba" are the bad chars because they tend to corrupt the char after so that is what was tested

!mona jmp -r esp -cpb "\x00\x23\x3c\x83\xba"

I got the same jmp addresses as the OSCP 1 flag