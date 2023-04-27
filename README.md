# Bi

prac 1
AIM:- Perform Linear regression on a data warehous

data.

Step 1: Go to RStudio -> Click on file→→ New file -> go to Rscript

Step 2:

height <-c(151, 174, 135, 186, 128, 135, 179, 163, 152, 131)

weight <- c(63, 81, 56, 91, 47, 57, 76, 72, 62, 48)

height

4weight

print(height)

relation<-Im(weight height)

print(relation)

print(summary(relation))

ac-data.frame(height=170)

result-predict[relation,a)

print(result)

plot(height, weight,col="blue",main="height and weight regression",

abline[relation),cex=3,pch=16,xlab="height in cm", ylab="weight in kg")








Practical 2

AIM: Perform Linear regression on a data warehous

Step1:Go to R studio create file→

Step2: Install catools → go to tools click on install package →→ write package name then click on install. quality=read.csv("C:\\Program Files\\RStudio\\quality_prac.csv")

str(quality)

summary(quality)

table(qualitySPoorCare)

install.packages("caTools")

library(caTools)

set.seed(88)

split-sample.split(quality$PoorCare,SplitRatio = 0.75)

split

qualityTrain-subset(quality,split=TRUE) qualityTest subset(quality,split=FALSE)

numquality<-quality.c(-1,-12)]

head(numquality) cor(numquality)

Qualitylog-gim(PoorCare Office Visits+Narcotics, data = qualityTrain,family = binomial)

summary(Qualitylog)

#make predictions on training set

predictTrain=predict(Qualitylog,type="response")

summary(predictTrain)

tapply(predictTrain, quality$PoorCare, mean)

table(quality$PoorCare,predictTrain>0.5)

install.packages("ROCR")

library(ROCR)

ROCRpred prediction(predict Train,quality$PoorCare)

ROCRperf-performance(ROCRpred, "tpr","for")

plot(ROCRperf,colorize=TRUE)




Practical 3

AIM: Perform data classification using classification

algorithm

Naive-bayes:-

Step1:Go to R studio-create file→

Step2: Install catools, e1071,caret→ go to tools click on install package write package name then click on Install

Step3:

#classification using NAIVE BAYES THEOREM

data("iris")

str(iris)

install.packages("e1071") #predict function

install.packages("caTools")

install.packages("caret") library(e1071)

library(caTools)

library(caret)

splite-sample.split(iris,SplitRatio = 0.7)

split

train_clc-subset(iris,split=TRUE)

test_cle-subset(iris,split=FALSE)

View(iris)

train_scale-c-scale(train_cl[,1:4])

rotest scalec-scale(test_cll,1:4])

View(train_scale)

set.seed(120)

(classifier_de-naive Bayes(Species,data=train_cl)

Y pred<-predict(classifier_cl,test_cl)

Y pred

2 cm<-table(test_c$Species,y_pred)

72cm

confusionMatrix(cm)


