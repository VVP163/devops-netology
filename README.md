# devops-netology
Learning Netology course DevOps
Me First Commit!
Описание игнорируемых файлов описанных в .gitignore расположенного в папке Terraform
1. **/.terraform/* - все файлы в папке ".terraform" и не важно сколько каталогов до этой папки
2. *.tfstate - все файлы с "расширением" - tfstate (по шаблону "любые символы в любом количестве.tfstate") в папке с файлом .gitignore
3. *.tfstate.* - все файлы в название которых встречается конструкция "любые символы в любом количестве .tfstate.любые символы в любом количестве" в папке с файлом .gitignore
4. crash.log - файл crash.log в папке с файлом .gitignore
5. crash.*.log - файлы crash."любые символы в любом количестве".log в папке с файлом .gitignore в  папке с файлом .gitignore
6. *.tfvars - все файлы в названиях которых встречается конструкция "любые символы в любом количестве.tfvars" в папке с файлом .gitignore
7. *.tfvars.json - все файлы в названиях которых встречается конструкция "любые символы в любом количестве.tfvars.json" в папке с файлом .gitignore
8. override.tf - файл override.tf в папке с файлом .gitignore
9. override.tf.json - файл override.tf.json в папке с файлом .gitignore
10. *_override.tf - все файлы в названиях которых встречается конструкция "любые символы в любом количестве_override.tf" в папке с файлом .gitignore
11. *_override.tf.json - все файлы в названиях которых встречается конструкция "любые символы в любом количестве_override.tf.json" в папке с файлом .gitignore
12. .terraformrc - файл .terraformrc в папке с файлом .gitignore
13. terraform.rc - файл terraform.rc в папке с файлом .gitignore
New line in branch fix
