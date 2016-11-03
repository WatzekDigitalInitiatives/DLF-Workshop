## Navigate the computer

```
ls
cd agalma
ls
cd scratch
```

## Phylogenetic Pipeline

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

## Download reports

**For Mac:**

1. Exit the cloud computer by **typing** `exit`

2. **Copy** and **paste** the following command on your terminal:  **Note: Do not hit return yet**

  ```
  scp -rp -i dlf-workshop-key.pem ubuntu@
  ```
3. Go to Amazon Console and **copy** your Public IP like we did before (select your row and copy the number under Public IP column)
4. **Paste** it at the end of your command you just typed. **Note: Do not hit return yet**
5. **Copy** the following and **paste** it at the end of the IP address you just pasted

  ```
  :~/agalma/reports/DLF_Phylogeny ~/Desktop/
  ```
6. Your final command should look like this with `xx.xx.xx.xx` replaced by your IP address:

  ```
  scp -rp -i dlf-workshop-key.pem ubuntu@xx.xx.xx.xx:~/agalma/reports/DLF_Phylogeny ~/Desktop/
  ```
7. **Hit** return now to download the reports

**For Windows:**

1. On the side bar of the mobaXterm **double click** on `agalma`
2. **Double click** on `reports` folder
3. **Drag and drop** `DLF_Phylogeny` folder on your Desktop

## Open reports

- Navigate to your `Desktop` and to `DLF_Phylogeny` folder
- Double click on `index.html` file
