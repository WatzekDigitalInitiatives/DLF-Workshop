## Catalog

```
cd data
agalma catalog insert --id SRX288285 --paths SRX288285_1.fq SRX288285_2.fq --species "Agalma elegans" --ncbi_id 316166
agalma catalog insert --id SRX288432 --paths SRX288432_1.fq SRX288432_2.fq --species "Craseoa lathetica" --ncbi_id 316205
agalma catalog insert --id SRX288431 --paths SRX288431_1.fq SRX288431_2.fq --species "Physalia physalis" --ncbi_id 168775
agalma catalog insert --id SRX288430 --paths SRX288430_1.fq SRX288430_2.fq --species "Nanomia bijuga" --ncbi_id 168759
agalma catalog insert --id JGI_NEMVEC --paths JGI_NEMVEC.fa --species "Nematostella vectensis" --ncbi_id 45351
```

## Post-assemble

```
cd ../scratch
agalma postassemble --id SRX288285 --assembly ../data/SRX288285.fa
agalma postassemble --id SRX288430 --assembly ../data/SRX288430.fa
agalma postassemble --id SRX288431 --assembly ../data/SRX288431.fa
agalma postassemble --id SRX288432 --assembly ../data/SRX288432.fa
agalma postassemble --id JGI_NEMVEC --external
```

## Load

```
agalma load --id SRX288285
agalma load --id SRX288430
agalma load --id SRX288431
agalma load --id SRX288432
agalma load --id JGI_NEMVEC
```

**Check load IDs**
`agalma diagnostics list`

**Export load IDs**
`export LOAD_IDS=$("6, 7, 8, 9, 10")`

## Phylogenetic Pipeline

**Homologize**
`agalma homologize --id DLF_Phylogeny $LOAD_IDS`

**Multalign**
`agalma multalign --id DLF_Phylogeny`

**Genetree**
`agalma genetree --id DLF_Phylogeny`

**Treeprune**
`agalma treeprune --id DLF_Phylogeny`

**Multalign**
`agalma multalign --id DLF_Phylogeny`

**Supermatrix**
`agalma supermatrix --id DLF_Phylogeny`

**Speciestree**
`agalma speciestree --id DLF_Phylogeny --raxml_flags="-o Nematostella_vectensis"`

## Generate Reports

```
cd ..
agalma report --id DLF_Phylogeny --outdir reports/DLF_Phylogeny
agalma resources --id DLF_Phylogeny --outdir reports/DLF_Phylogeny
agalma phylogeny_report --id DLF_Phylogeny --outdir reports/DLF_Phylogeny
```

## Download reports
```

```
