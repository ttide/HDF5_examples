Examples of making basic meshes with scalar and vector data in HDF5.

Examples are in C++, but use the HDF5 C api. 
Examples were built and tested against HDF5 1.8.18, but should work with older versions.

Makefiles assume h5c++ is in $PATH.

orthonormalgrids/ - examples of 3D orthogonal, unit dx,dy,dz meshes. The mesh coordinates are implicit. Equivalent to a vtkImageData dataset.

orthonormalgrids/scalar/ - writes a mesh with a single scalar. The output .h5 can be read directly by the Pixie reader in VisIt/ParaView. An XDMF is added only for illustration.

orthonormalgrids/vector_comps/ - writes a mesh with a single vector, where the vector components are written as separate arrays. The .h5 can be read with the Pixie reader, but the vector will have to be reconstituted in the vis application. The XDMF file can be read by ParaView.

orthonormalgrids/vector_interleaved/ - writes a mesh with a single vector, where the vector components are written as x,y,z triples. The .h5 can NOT be read with the Pixie reader. The XDMF file can be read by VisIt and ParaView.

rectilineargrids/ - examples of 3D orthogonal, aribtrary x,y,z coordinate spacing meshes. Equivalent to a vtkRectilinearGrid data set.

rectilineargrids/scalar/ - writes a mesh with a single scalar. The XDMF can be read by both VisIt and ParaView.

curvilineargrids/ - examples of 3D curvilinear grids. Equivalent to vtkStructuredGrid data sets.

curvilineargrids/scalar/ - writes a cylindrical structured mesh with a single scalar. The XDMF can be read by both VisIt and ParaView.
