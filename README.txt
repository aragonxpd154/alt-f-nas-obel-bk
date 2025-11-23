🔁 RESTAURAÇÃO

Para restaurar totalmente o sistema:

1) Restaurar overlay Alt-F:

tar -xvzf altf-root-overlay.tar.gz -C

(Isso reescreve /mnt/md0/Alt-F com todos os arquivos.)

2) Restaurar configs runtime:

tar -xvzf etc-runtime.tar.gz -C 

3) Restaurar interface:

tar -xvzf web-ui.tar.gz -C 

4) Restaurar NAND (caso desastre geral):

dd if=mtd0_bootloader.bin of=/dev/mtd0
dd if=mtd1_kernel.bin of=/dev/mtd1
dd if=mtd2_rootfs.bin of=/dev/mtd2



