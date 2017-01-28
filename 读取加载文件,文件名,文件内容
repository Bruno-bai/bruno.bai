def loadData(direction):
    trainfileList=listdir('F:\\MachineLearning-master\\logistic regression\\use Python and NumPy\\train')#返回文件夹下的所有文件列表矩阵
    m=len(trainfileList)
    dataArray= zeros((m,1024))
    labelArray= zeros((m,1))
    for i in range(m):
        returnArray=zeros((1,1024))  #每个txt文件形成的特征向量
        filename=trainfileList[i]
        fr=open('%s/%s' %(direction,filename))
        for j in range(32):
            lineStr=fr.readline()
            for k in range(32):
                returnArray[0,32*j+k]=int(lineStr[k])
        dataArray[i,:]=returnArray   #存储特征向量
    
        filename0=filename.split('.')[0]
        label=filename0.split('_')[0]
        labelArray[i]=int(label)     #存储类别
    return dataArray,labelArray
