# Write and rename a Single File in Databricks pyspark to AzureBlob
#listar partiçoes


d=dbutils.fs.ls('mount to blob')




![image](https://user-images.githubusercontent.com/84607692/158750752-0bf916f1-04c1-45b9-a02f-05dfd96af0ec.png)





d=list(d)


#Identificar e renomear o arquivo no blob com o comando abaixo



for i in d[3:4]:

    c=i[0]
    
    dbutils.fs.mv(c,'fileName')
    
    
    
    
    
#Identificar e apagar o arquivo criado no blob sucessivamente com o comando abaixo




for i in d[0:1]:

    dbutils.fs.rm(i[0])
