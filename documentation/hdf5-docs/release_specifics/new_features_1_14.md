---
title: New Features in HDF5 1.14
redirect_from: 
  - display/HDF5/New+Features+in+HDF5+Release+1.14
---

# New Features in HDF5 1.14

HDF5 Release 1.14.0 is the final released version of all the features that were released in 1.13.0-1.13.3.  Thus, the new features in the HDF4 1.14 release include:

* [Asynchronous I/O operations](asyn_ops_wHDF5_VOL_connectors.md)
HDF5 provides asynchronous APIs for the HDF5 VOL connectors that
support asynchronous HDF5 operations using the HDF5 Event Set (H5ES)
API. This allows I/O to proceed in the background while the application
is performing other tasks.

* [Subfiling VFD](http://docs.hdfgroup.org/hdf5/rfc/RFC_VFD_subfiling_200424.pdf)
The basic idea behind sub-filing is to find the middle ground between
single shared file and one file per process - thereby avoiding some
of the complexity of one file per process, and minimizing the locking
issues of a single shared file on a parallel file system.

* [Onion VFD](https://docs.hdfgroup.org/hdf5/rfc/Onion_VFD_RFC_211122.pdf)
There is a desire to introduce and track modifications to an HDF5 file
while preserving or having access to the file as it existed prior to a
particular set of modifications. To this end, this RFC proposes an Onion
Virtual File Driver (VFD) as an effectively in-file revision management
facility. Users will be able to open a particular revision of the file,
read from and make modifications to the file, and write to file as a new
revision. The name "Onion" derives from a mnemonic: the original file
exists with data layered atop one another from an original file to the
most recent revision

* [Multi Dataset I/O](https://docs.hdfgroup.org/hdf5/rfc/H5HPC_MultiDset_RW_IO_RFC.pdf)
The HDF5 library allows a data access operation to access one dataset at
a time, whether access is collective or independent. However, accessing
multiple datasets will require the user to issue an I/O call for each
dataset. This release provides a set of new routines that allow users
to access multiple datasets with a single I/O call.

* [New tools h5dwalk and h5delete]()
The new tool h5dwalk provides parallelism for improved performance while
also including critical logging capabilities to capture outputs from
applying the serial tools over large collections of HDF5 files.

 
