# read_OU_mtx library is to read single cell raw data in C4 platform
#read_ou_mtx is a very easy tool to solve when you raw data is not 10X.
#var_names = genes[1].values error
#It appears there is no second column in your genes.tsv file, which is causing this error. Can you retry the command with the gene.column #argument set to 1 and let me know if it works? e.g.

#In R seurat package ,you can use Read10X("same_directory", gene.column=1),but we have not same function in scanpy.
#so we write read_ou_mtx function that can  solve it.
you can use in python scripts
!pip install read_OU_mtx
from read_OU_mtx import read_OU_mtx
adata=read_OU_mtx(
    "./data/filtered_gene_bc_matrices/hg19/",  # the directory with the `.mtx` file
   
    var_names='gene_symbols',
    make_unique=True    
)
adata
