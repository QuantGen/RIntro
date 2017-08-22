### Brief Introduction to R


## Topics
----------------------------------------------
[1. Installation](###installation)

-------------------------------------------


```r
h2=c(.1,.05,.01)
cols=c(4,2,1)

for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}

i=1
load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))


for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}


h2=c(.1,.05,.01)
cols=c(4,2,1)

for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}

i=1
load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))


for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}


h2=c(.1,.05,.01)
cols=c(4,2,1)

for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}

i=1
load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))


for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}


h2=c(.1,.05,.01)
cols=c(4,2,1)

for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}

i=1
load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))


for(i in 1:length(h2)){
   load(paste0('../output/pc_adj/h2_',h2[i],'/result50K.RData'))
   if(i==1){
   		Y=matrix(ncol=length(h2),nrow=ncol(reject))
   		x=as.integer(colnames(reject))
   		colnames(Y)=h2
   		rownames(Y)=x
   		plot(numeric()~numeric(),xlim=range(x),ylim=c(.045,.1),ylab='Rejection Rate',xlab='Lag between markers (# of SNPs)')
   		abline(h=.05,lty=2)
   }
   Y[,i]=colMeans(reject,na.rm=T)
   lines(x=x,y=Y[,i],col=cols[i])
   points(x=x,y=Y[,i],col=cols[i])
   text(x=3500,y=c(.095,.092,.089)[i],label=paste0('h2=',h2[i]),col=cols[i])

}



```

## 1. Installation

[menu](#Topics)


## 2. Types


## 3. Arrays

#### 3.1. Vectors

#### 3.2. Matrices

#### 3.3. Multi dimensional (homogeneous) arrays


#### 3.4 Lists

#### 3.5 Data Frames





