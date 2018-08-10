# meme-results
Report of MEME Suite 5.0.1 results

# Data
TF: CTCF; cell-type: GM12878

pos.fa.masked: 5000 IDR optimal peaks, central region 400bp

neg.fa.masked: 5000 sequences of 400bp

# Code Command
module load meme/5.0.1

meme-chip -neg ~/TF_data/CTCF/meme_data/neg.fa.masked -o memechip_out -meme-minw 5 -meme-maxw 50 -meme-nmotifs 10 ~/TF_data/CTCF/meme_data/pos.fa.masked


# Error message
Fatal error in MPI_Allreduce: Internal MPI error!, error stack:    

MPI_Allreduce(912).......: MPI_Allreduce(sbuf=0x7fffe6d0cad0, rbuf=0x7fffe6d0cb10, count=1, dtype=USER<contig>, op=0x98000001, MPI_COMM_WORLD) failed                                                                                           
  MPIR_Allreduce_impl(769).:                                                                                              MPIR_Allreduce_intra(330):                                                                                              MPIR_Localcopy(123)......: memcpy arguments alias each other, dst=0x7fffe6d0cb10 src=0x7fffe6d0cad0 len=72  
