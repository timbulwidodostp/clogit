# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Conditional Logistic Regression Use Package clogit And clogistic With (In) R Software
# Install Conditional Logistic Regression Use Package clogit And clogistic With (In) R Software
install.packages("readxl")
install.packages("httr")
install.packages("survival")
install.packages("mgcv")
install.packages("Epi")
library("httr")
library("readxl")
library("survival")
library("mgcv")
library("Epi")
# Import Data Excel Into R From Github Olah Data Semarang (timbulwidodostp)
github_link <- "https://github.com/timbulwidodostp/clogit/raw/main/clogit/clogit.xlsx"
temp_file <- tempfile(fileext = ".xlsx")
req <- GET(github_link, 
# authenticate using GITHUB_PAT
authenticate(Sys.getenv("GITHUB_PAT"), ""),
# write result to disk
write_disk(path = temp_file))
clogit <- readxl::read_excel(temp_file)
# Estimate Conditional Logistic Regression Use Package clogit And clogistic With (In) R Software
clogistic(Dependen ~ Independen_1 + Independen_2, strata = Id, data = clogit)
clogit(Dependen ~ Independen_1 + Independen_2 + strata(Id), clogit)
# Conditional Logistic Regression Use Package clogit And clogistic With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
