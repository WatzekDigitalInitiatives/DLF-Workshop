## Navigate the computer

```
ls
cd agalma
ls
cd scratch
ls
```

## Phylogenetic Pipeline

**Genetree**

```
agalma genetree --id DLF_Phylogeny
```

**Treeprune**

```
agalma treeprune --id DLF_Phylogeny
```

**Multalign**

```
agalma multalign --id DLF_Phylogeny
```

**Supermatrix**

```
agalma supermatrix --id DLF_Phylogeny
```

**Speciestree**

```
agalma speciestree --id DLF_Phylogeny --raxml_flags="-o Nematostella_vectensis"
```

## Generate Reports

```
cd ..
agalma report --id DLF_Phylogeny --outdir reports/DLF_Phylogeny
agalma resources --id DLF_Phylogeny --outdir reports/DLF_Phylogeny
agalma phylogeny_report --id DLF_Phylogeny --outdir reports/DLF_Phylogeny
```

## Exit your EC2 Instance

```
exit
```

## Download reports

**For Mac:**
- Replace `xx.xx.xxx.xxx` with your public IP address from AWS console
- On terminal you will see `myAccount@myComputerName:~$` and your computer name is `myComputerName`
- Replace `yourComputerName` with your own computer name.
- Run the following command with proper replacement for PublicIP and Computer Name
```
scp -rp -i dlf-workshop-key.pem ubuntu@xx.xx.xxx.xxx:/agalma/reports/DLF_Phylogeny /Users/yourComputerName/Desktop/
```

**For Windows**
- On the side bar of the mobaXterm double click on `agalma`
- Navigate to `reports` folder
- Drag and drop `DLF_Phylogeny` folder on your Desktop

## Open reports

- Navigate to your `Desktop` folder and to `DLF_Phylogeny` folder
- Double click on `index.html` file
