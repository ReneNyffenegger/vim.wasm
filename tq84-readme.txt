sudo apt install -y emscripten

./build.sh
   …
configure: error: cannot run C compiled programs.
If you meant to cross compile, use `--host'.
See `config.log' for more details

    ==> added 
        --host=x86_64 \
    in build.sh
       (The value of x86_64 is the result of
          uname -m
       ) 

./build
   …
checking whether toupper is broken... configure: error: cross-compiling: please set 'vim_cv_toupper_broken'

    ==> add in configure command (build.sh)
        vim_cv_toupper_broken=set


./build.sh
   …
checking whether we talk terminfo... configure: error: cross-compiling: please set 'vim_cv_terminfo'

  ---

./build.sh
   …
build.sh: Copying bitcode to wasm/
cp: cannot stat 'src/vim.bc': No such file or directory

