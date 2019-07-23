Command for running Maker
==

```
base="Peromyscus_nudipes"
genome="$SHARE/pero_genomes/"$base"/genome/Pnud_10x_v1.fasta"

mkdir -p $SHARE/pero_genomes/"$base"/genome/maker
cd $SHARE/pero_genomes/"$base"/genome/maker

mpiexec -n 48 $HOME/test/maker/bin/maker \
-fix_nucleotides -base "$base" -quiet \
-genome "$genome" \
/mnt/lustre/macmaneslab/macmanes/maker_control_files/maker_opts.ctl \
/mnt/lustre/macmaneslab/macmanes/maker_control_files/maker_bopts.ctl \
/mnt/lustre/macmaneslab/macmanes/maker_control_files/maker_exe.ctl
```
