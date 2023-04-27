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






