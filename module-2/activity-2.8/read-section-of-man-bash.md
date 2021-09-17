       read [-ers] [-a aname] [-d delim] [-i text] [-n nchars] [-N nchars] [-p prompt] [-t timeout] [-u fd] [name ...]
              One  line  is read from the standard input, or from the file descriptor fd supplied as an argument to the -u option, split into words as described above under Word Splitting, and the first word is assigned to the first
              name, the second word to the second name, and so on.  If there are more words than names, the remaining words and their intervening delimiters are assigned to the last name.  If there are fewer words read from the  in‐
              put  stream  than  names, the remaining names are assigned empty values.  The characters in IFS are used to split the line into words using the same rules the shell uses for expansion (described above under Word Split‐
              ting).  The backslash character (\) may be used to remove any special meaning for the next character read and for line continuation.  Options, if supplied, have the following meanings:
              -a aname
                     The words are assigned to sequential indices of the array variable aname, starting at 0.  aname is unset before any new values are assigned.  Other name arguments are ignored.
              -d delim
                     The first character of delim is used to terminate the input line, rather than newline.  If delim is the empty string, read will terminate a line when it reads a NUL character.
              -e     If the standard input is coming from a terminal, readline (see READLINE above) is used to obtain the line.  Readline uses the current (or default, if line editing was not previously active) editing settings, but
                     uses Readline's default filename completion.
              -i text
                     If readline is being used to read the line, text is placed into the editing buffer before editing begins.
              -n nchars
                     read returns after reading nchars characters rather than waiting for a complete line of input, but honors a delimiter if fewer than nchars characters are read before the delimiter.
              -N nchars
                     read  returns after reading exactly nchars characters rather than waiting for a complete line of input, unless EOF is encountered or read times out.  Delimiter characters encountered in the input are not treated
                     specially and do not cause read to return until nchars characters are read.  The result is not split on the characters in IFS; the intent is that the variable is assigned exactly the characters  read  (with  the
                     exception of backslash; see the -r option below).
              -p prompt
                     Display prompt on standard error, without a trailing newline, before attempting to read any input.  The prompt is displayed only if input is coming from a terminal.
              -r     Backslash does not act as an escape character.  The backslash is considered to be part of the line.  In particular, a backslash-newline pair may not then be used as a line continuation.
              -s     Silent mode.  If input is coming from a terminal, characters are not echoed.
              -t timeout
                     Cause  read to time out and return failure if a complete line of input (or a specified number of characters) is not read within timeout seconds.  timeout may be a decimal number with a fractional portion follow‐
                     ing the decimal point.  This option is only effective if read is reading input from a terminal, pipe, or other special file; it has no effect when reading from regular files.  If read times out, read  saves  any
                     partial  input  read  into  the specified variable name.  If timeout is 0, read returns immediately, without trying to read any data.  The exit status is 0 if input is available on the specified file descriptor,
                     non-zero otherwise.  The exit status is greater than 128 if the timeout is exceeded.
              -u fd  Read input from file descriptor fd.

              If no names are supplied, the line read, without the ending delimiter but otherwise unmodified, is assigned to the variable REPLY.  The exit status is zero, unless end-of-file is encountered, read times out  (in  which
              case the status is greater than 128), a variable assignment error (such as assigning to a readonly variable) occurs, or an invalid file descriptor is supplied as the argument to -u.
