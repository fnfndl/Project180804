install.packages("rJava")
install.packages("DBI")
install.packages("RJDBC")
install.packages("XML")
install.packages("memoise")
install.packages("KoNLP")
install.packages("wordcloud")
install.packages("dplyr")
install.packages("ggplot2")
install.packages("ggmap")
install.packages("rvest")
install.packages("RColorBrewer")
install.packages("data.table")
install.packages("dplyr")
install.packages("reshape")

 library(rJava)
 library(DBI)
 library(RJDBC)
 library(XML)
 library(memoise)
 library(KoNLP)
 library(wordcloud)
 library(dplyr)
 library(ggplot2)
 library(ggmap)
 library(rvest)
 library(RColorBrewer)
 library(data.table)
 library(reshape)

getwd()

KoNLP::useSejongDic
dSeoulNew <- readLines("Seoul_new.txt")
class(dSeoulNew) #현재 클래스는 'Character'

dSeoulNew <-sapply(dSeoulNew, extractNoun, USE.NAMES =T) ##명사추출
class(dSeoulNew)

##gsub : 문자열을 쪼개는 것 
## //d+ : Decimal 특정한 형태의 값을 의미 (자릿수는 상관 없음)
dSeoulNew<-gsub("//d+","",dSeoulNew) ##숫자제거
head(dSeoulNew)

dSeoulNew <-unlist(dSeoulNew)
class(dSeoulNew)

write(dSeoulNew,"Seoul_new2.txt") ##공백제거
dSeoulNew <- read.table("Seoul_new2.txt") ##테이블 구조로 변경



