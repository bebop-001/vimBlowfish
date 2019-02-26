
Tue Feb 26 09:25:31 PST 2019

This is a command line tool for encrypting and decrypting text files
in vim's blowfish-2 format.

From USAGE on the tool:
USAGE: vimBlowfish [-t -s -f] inFile outFile [password]
  -t  Run the selftest, print results and exit
  -s  Run the selftest, print results and and save to files, then
      exit
  -f  force write to the output file if it exists.  If not set and the
      output file exists, we abort.
  inFile   the input file
  outFile  the output file
  password the encrypt/decrypt password.  Optional unless inFile or outFile
     is stdin opr stdout.
     We examine the input file and if it is a non-encrypted file, we 
  encrypt the result and send it to outFile.  Likewise, if the input
  is encrypted we decrypt and send the output to outFile.
     '-' for inFile/outFile means send input/output to stdin/stdout.
     If inFile or outFile is to stdin/stdout, a command line password
  must be supplied.


There are several versions of vimdecrypt on github.  The one I
looked at mostly was https://github.com/gertjanvanzwieten/vimdecrypt.
Without Gertjan van Zwieten's example, I would never have been
able to figure out how to do this.  Thank you Gertjan!

The tool requires the PyCrypto library.

The tool was written on Linux and I have not tried to run it
under Windows or IOS.  If you port it to another OS and would
like your changes incorporated here, please let me know.
Likewise, if you discover bugs in the code, please let me know.

Steve Smith
