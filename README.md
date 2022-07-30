# Libc Diff

In this experiment we want to see how libc changes in different:

 - operating systems
 - operating system versions

And so we will use a matrix of containers to grab a libc variant in each, save to an
artifact, and then compare between all of them. Since libc by default does not have debug info, the
easiest thing to do is use libabigail for the comparison, which will do basic checking for
changed or missing symbols.

Big picture goal:
 
> to figure out whether we can reuse the binaries from the AWS-spack binary cache on TOSS3 clusters.
