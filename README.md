# Greyatom IDE's Tree View

This fork of [Tree View package](https://github.com/learn-co/learn-ide-tree) is used by the [Greyatom IDE](https://greyatom.co) to provide all of tree-view's functionality while synchronizing with a remote filesystem. It's intended to be used alongside the primary [Grey IDE package](https://github.com/PradeepJaiswar/greyatom-ide).

## Methodology
For an understanding of how tree-view works, see [it's repo](https://github.com/atom/tree-view).

This minimal amount of change is primarily accomplished by using the [nsync-fs]() module, which provides an fs interface to meet the usage of fs throughout the tree-view package. In other words, this pacakge simply intercepts tree-view's calls to the physical filesystem, and routes them to the virtual filesystem maintained by the `nsync-fs` module. Most other functionality of the package is left unchanged.
