## Navigate the computer

```
ls
cd agalma
ls
cd scratch
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
1. Copy the following command on your terminal:  **Note: Do not hit return yet**
  ```
  scp -rp -i dlf-workshop-key.pem ubuntu@
  ```
- Go to Amazon Console and copy your Public IP like we did before (select your row and copy the number under Public IP column)
- Paste it at the end of your command you just typed:
- Copy the following and add it at the end of the IP address you just pasted
  ```
  :~/agalma/reports/DLF_Phylogeny ~/Desktop/
  ```
- Your final command should look like this with `xx.xx.xx.xx` replaced by your IP address:
  ```
  scp -rp -i dlf-workshop-key.pem ubuntu@xx.xx.xx.xx:~/agalma/reports/DLF_Phylogeny ~/Desktop/
  ```

**For Windows**
- On the side bar of the mobaXterm double click on `agalma`
- Navigate to `reports` folder
- Drag and drop `DLF_Phylogeny` folder on your Desktop

## Open reports

- Navigate to your `Desktop` folder and to `DLF_Phylogeny` folder
- Double click on `index.html` file
