# vcfR_win-builder
Precompiled binary of vcfR for Windows users



Some Windows users may not want to try to compile the source for vcfR.
For these people I have provided this precompiled binary.
Download it to a local directory, open R and use the following command to install.

    install.packages("./vcfR_0.1.zip", repos = NULL)


This example assumes the *.zip archive is in your working directory.


This version built on 2015-11-23



# adegenet development version

The constructor for the adegenet genlight object calls mclapply to facilitate multithreading by using forks.
Forks do not exist in Windows, so this throws an error.
I've created a version of adegenet which sets n.cores to one so that Windows users will not throw an error when they use this function.
They won't be able to multithread either.
I've issued a pull request with the adegenet people.
In the mean time, I've placed my version here.
In general, I do not recommend using this version.
But if you are specifically interested in the problem of using mclapply in Windows, this may be a solution.

This version built 2015-11-23


