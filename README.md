# helloword
làm đồ án thi
###### Nhập thông tin khách hàng:
a = int(input("Nhập mã số khách hàng: "))
b = str(input("Nhập địa chỉ khách hàng: "))
while True:
    name = input("Hãy Nhập tên: ")  
    n = name.split(' ') 
    for i in range(len(n)): 
        if(not (n[i].isalpha()) or (n[i].isdigit())):  
            print("Hãy nhập lại!!!!!") 
            break #  
    else: 
        print("Họ và tên khách  hàng: ", ' '.join(n)) 
        break
while True:
    v = input("Nhập Số Điện Thoại: ") 
    if (len(v) > 10 or len(v) < 10):
        print("---Vui lòng nhập lại---")
    else:
        print("----> Số Điện Thoại khách hàng: ",v) 
        print("----> Mã số khách hàng: ",a)
        print("----> Địa chỉ khách hàng: ",b)
        break 
#------------------------------------------------------------------------------------------------------
#số kw tiêu thụ:
tieu_thu = int
csc = int(input("+ Nhập chỉ số cũ: "))
while csc<0:
    print("Vui lòng nhập lại số nguyên lớn hơn 0!!!!")
    csc = int(input("+ Nhập chỉ số cũ: "))
else:
    csm = int(input("+ Nhập chỉ số mới: "))
    if csm<0:
        print("Vui lòng nhập lại số nguyên lớn hơn 0!!!!")  
        csm = int(input("+ Nhập chỉ số mới: "))
    else:    
        tieuthu = abs(csm-csc)
        print("-->",name,"tiêu thụ khoảng",format(tieuthu,","),"kw")
#------------------------------------------------------------------------------------------------------
#số tiền tạm tính:
I= 1500; II= 1800; III= 2000; IV= 2500; V= 3500
tam_tinh = int
if (tieuthu<=30):
    print("-->Số kw tiêu thụ là ",format(tieuthu,","),"kw thuộc định mức I")
    tam_tinh= tieuthu*I
    print("-->Số tiền tạm tính: ",format(tam_tinh,","),"đồng")
else:
    if (30<tieuthu<=50):
        print("-->Số kw tiêu thụ là ",format(tieuthu,","),"kw thuộc định mức II")
        tam_tinh= tieuthu*II
        print("-->Số tiền phải trả: ",format(tam_tinh,","),"đồng")
    else:
        if (50<tieuthu<=100):
            print("-->Số kw tiêu thụ là ",format(tieuthu,","),"kw thuộc định mức III")
            tam_tinh= tieuthu*III
            print("-->Số tiền phải trả: ",format(tam_tinh,","),"đồng")
        else:
            if (100<tieuthu<=150):
                print("-->Số kw tiêu thụ là ",format(tieuthu,","),"kw thuộc định mức IV")
                tam_tinh= tieuthu*IV
                print("-->Số tiền phải trả: ",format(tam_tinh,","),"đồng")
            else:
                print("-->Số kw tiêu thụ là ",format(tieuthu,","),"kw thuộc định mức V")
                tam_tinh= tieuthu*V
                print("-->Số tiền phải trả: ",format(tam_tinh,","),"đồng")                                                             
#------------------------------------------------------------------------------------------------------                                
#số tiền thêm phụ phí:
if tam_tinh > 300000:
    phaitra = tam_tinh+tam_tinh*0.3
    print("-->Số tiền phải trả khi có phụ phí là: ",format(phaitra,","),"đồng")  
else:
    print("-->Số tiền phải trả khi có phụ phí là:",format(tam_tinh,","),"đồng")
    if tam_tinh > 500000:
        phaitra = tam_tinh+tam_tinh*0.8
        print("-->Số tiền phải trả khi có phụ phí là:",format(phaitra,","),"đồng")
    else:
        if tam_tinh > 1000000:
            phaitra = tam_tinh+tam_tinh*1.1
            print("-->Số tiền phải trả khi có phụ phí là:",format(phaitra,","),"đồng")   
