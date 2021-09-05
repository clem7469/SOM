sexe = c(rep("Femmes",28),rep("Hommes",16))
age = c(64, 79, 67, 64, 72, 72, 66, 53, 65, 45, 49, 51, 57, 63, 47, 50, 75, 22, 58, 58, 51, 42, 70, 47, 54, 49, 46, 26, 59, 50, 68, 29, 58, 69, 60, 46, 48, 48, 64, 61, 69, 74, 58, 62)
genre = c(rep(1,28),rep(2,16))

————————
Age moyen cas cliniques inclus

donnees = data.frame(sexe, age, genre)
summary(donnees)

————————
Proportion des hommes des cas cliniques inclus

mean(Hommes)

————————
Proportion des femmes des cas cliniques inclus

mean(Femmes)

————————
Type de cancer 

typecancer<-data.frame(x1=c(1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1),x2=c("CBPC","CBPC", "Gyn","CBPC","CBPC","CBPC","UNCT","Gyn","Dig","Hemato","Thyroide","CBPC","CBPC","Hemato","Gyn","Gyn","CBPC","Gyn","CBNPC","CBPC","CBNPC","Dig","ORL","Dig","CBPC","Hemato","Gyn","CBPC","ORL","CBPC","CBPC","Gyn","CBPC","UNCT","ORL","Gyn","CBPC","Gyn","Mesothelium","CBPC","CBPC","CBPC","CBPC","Gyn"))
table(typecancer$x2)
prop.table(table(typecancer$x2))
barplot(prop.table(table(typecancer$x2)),xlab="Cancer",ylab="Proportion")

————————
Auto-anticorps
anticorps<-data.frame(x1=c(1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1),x2=c(" Negatif","ANA","Ri"," Negatif","VGCC"," Negatif"," Negatif","Ri","VGKC"," Negatif"," Negatif"," Negatif"," Negatif"," N.S."," N.S."," Negatif"," N.S.","Ri"," Negatif"," N.S.","Ri"," Negatif"," Negatif","GAD"," Negatif"," Negatif","Ri","AMA"," Negatif"," Negatif"," Negatif"," Negatif","ANA","Ri"," Negatif","Ri","Hu","Ri"," Negatif"," N.S.","CV2"," N.S.","CaspR"," Negatif"))
table(anticorps$x2)
prop.table(table(anticorps$x2))
barplot(prop.table(table(anticorps$x2)),xlab="Cancer",ylab="Proportion")
