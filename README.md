#reading the csv data of student study hours and percentage scores#
student<-read.csv("https://raw.githubusercontent.com/AdiPersonalWorks/Random/master/student_scores%20-%20student_scores.csv")
print("reading the student data")
student

##assigning the values of Hours and Scores to y and x respectively##
x<-student$Scores
y<-student$Hours

##plotting the distribution of scores vs hours##
plot(x ~ Y)

##fit a linear regression model using function##
student.reg<-lm(x ~ y, data = student)

##put a regression line on plot##
abline(student.reg, col = "blue")

##summary of model##
print(summary(student.reg))

##predicting new values##
study_hour<-data.frame(Hours=9.25)

##computing the predicted results##
prediction<-predict(student.reg,study_hour)
print(prediction)
