# mktau
Installs TAU in user space, and creates a modulefile

## Developers and Maintainers
Kent Milfeld  (<mailto:milfeld@tacc.utexas.edu> include mktau in subject)

## mkmod Web Sites
* Github:        https://github.com/milfeld/mktau

## Description

Requires executions of the mktau script (3/4 times) with arguments.

```shell
       #you can cut and paste the instructions you need:
       
       cd; mkdir -p APPS; cd APPS    #create and go to an install directory
                                      # at TACC use $WORK (cd $WORK first)
                                      
       wget  https://raw.github.com/milfeld/mktau/master/mktau        #get mktau file
       wget  https://raw.github.com/milfeld/mktau/master/mktau_utils  #get mktau_utils
       wget  https://raw.github.com/milfeld/mktau/master/modules_help #get modulefile help
       chmod 700 mktau                                                #make mktau executable
      
       mktau  prep         # downloads latest pdt or tau tar files"
       mktau  pdt          # untars and builds pdt (required for instrumentation)"
       mktau  tau          # untars and builds tau"
       mktau  module       # creates and sets up personal module (modulefile)"
      
      # append "|& tee tau.log" to "mktau tau" for logging (similarly for others)
      # git clone https://github.com/milfeld/mktau   will download directory with mktau in it
```

## Code Access
To get access to the mkmod source code clone this repository:

    git clone https://github.com/milfeld/mktau
    
### mktau 0.9.1:
    1 Sets LIBGL_ALWAYS_INDIRECT=1  for paraprof display back to Mac X
    2 Include TACC module help file
    
### mktau 0.9.0:
    1 Designed to use intel 19.0.5 compiler (and its default MPI, impi).
    2 Change "comp_version=19.0.5" to particular version (at TACC)
    3 Execute "mktau" to get usage (mktau [prep | pdt | tau | module]
    4 Uses PAPI (a requirement at this point)
    
### TODO
    1 Make script work on non TACC-site systems (should not be difficult)
    2 Allow gcc compilation
    3 Allow non-PAPI installation

## Copyright
(C) 2018 University of Texas at Austin

## MIT License

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
