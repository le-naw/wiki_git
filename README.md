# gộp commit
git rebase -i HEAD~n <br>

n la số commit muốn gộp <br>
b2. để lại commit đầu là PICK, những cái sau replace PICK thành S <br>
lưu file <br>
b3. xem lại các comment của từng commit. Viết lại comment. <br>
lưu file <br>
b4. <br>
git push <br>

#Git ignore sẽ không có hiệu lực nếu file đã tồn tại trên repository trước đó. Để ignore các file đã được push lên từ trước, ta cần remove nó ra khỏi git bằng câu lệnh sau:<br>
	git rm -r --cached <tên file hoặc thư mục> <br>
Sau khi đã xoá file này bằng câu lệnh git rm, ta tiến hành liệt kê chúng vào gitignore và push lên. <br>

#Tạo mới repository, rồi clone, rồi tạo local repository, và ở trên local repository đó rồi thực hiện push thì cũng có trường hợp log như bên dưới được xuất ra. <br>
	$ git push No refs in common and none specified; doing nothing. Perhaps you 	should specify a branch such as 'master'. Everything up-to-date <br>
Cái này là do trên remote branch thì master branch chưa được tạo ra <br>
Cách giải quyết: cần thiết phải chỉ định rõ repository và branch. <br>
	 $ git push -u origin master <br>

#Thực hiện lệnh Push thì báo lỗi: <br>
	GIT push, HTTP code = 502 error <br>
Do dữ liệu đẩy lên quá lớn <br>
Thực hiện commant sau rồi push lại: <br>
	 git config http.postBuffer 524288000 #Set to 500MB <br>
   
#   
