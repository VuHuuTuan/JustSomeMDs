# Path
Đầu tiên ta cần biết các đặc điểm của cái hố này.


*******************************************************
*************************     *************************
**********************     A     **********************
*******************                 *******************
****************                       ****************
*************                             *************
**********                                   **********
*******                                         *******
****                              (Y)              ****
*     B                                         D     *
****                                               ****
*******                                         *******
**********                                   **********
*************                             *************
****************    (X)                ****************
*******************                 *******************
**********************     D     **********************
*************************     *************************
*******************************************************
 
- Dưới này đen thui, không có minimap và cần "Pin" để soi.
- "Pin" sẽ tiêu hao khi đi vào vùng tối. (tôi chưa confirm được di chuyển trong vùng sáng là tiêu hao ít Pin hay là không tiêu hao Pin)
- Lượng "Pin" còn lại được đại diện bằng vòng sáng trắng xung quanh nhân vật khi đứng gần vùng tối, càng nhỏ tức là sắp hết. (đi vài lầ)
- Có các điểm sáng Trắng ngẩu nhiên trên bản đồ có thể nạp thêm "Pin" (có 2 loại điểm sáng trắng, điểm sáng bé là cái ta cần, gặp vài lần là biết)
- Bản đồ có dạng hình thoi như trên, có 4 điểm event ở 4 góc (A, B, C, D) và nhiều thứ linh tinh khác (các event có thể là NPC, bãi quái, vườn, ổ đom đóm,...).
- Thường có các con đường bằng đom đóm nối đến các event này
- Dọc các con đường đom đóm thường có quái tương ứng (Nameless, Cultis,...), giết cũng có thể được đom đóm.
- Điểm spawn của ta là ngẩu nhiên (X hoặc Y như trên, hoặc bất kì đâu)
- Đánh giá lượng đom đóm nhận được
	+ nhặt đom đóm rải rác (trung bình)
	+ giết quái (ít - trung bình)
	+ ăn event (nhiều)

Để có nhiều đom đóm thì theo tôi nên ăn nhiều event nhất có thể, quái và đom đóm rải rác nhặt dọc đường là phụ.
Để ăn nhiều event thì phải xác định được vị trí của bản thân trên bản đồ để có thể xác định vị trí của các event dể dàng, ta cần tư duy định hướng 1 chút.

Cách xác định vị trí (Tây Bắc: TB, Đông Bắc: ĐB, Tây Nam: TN, Đông Nam: ĐN)

	+ Xác định bằng tường: Vì bản đồ là hình thoi, dựa vào vị trí của tường ta có thể xác định vị trí của bản thân trên bản đồ.
	+ Xác định bằng event: Khi đã ở 1 event, dựa vào hướng đi khi tiếp cận event ta có thể xác định bản thân đang ở hướng nào trên bản đồ.
	+ Thực tế: Vì là spawn ngẫu nhiên, sẽ có nhiều trường hợp xảy ra
		- Spawn ngay cạnh bản đồ, có tường -> áp dụng cách xác định vị trí bằng tường.
		Ví dụ: spawn tại X, điểm spawn có tường ở hướng TN, ta xác định mình đang ở hướng TN -> có 2 event ở gần đó hướng TB(B) và ĐN(D) so với điểm spawn.
			
		- Spawn ngay giữa bản đồ, không có tường, xem:
			+ Có đom đóm xung quanh -> đi theo đom đóm đến event bất kì, nhớ hướng đi.
			+ Không có đom đóm xung quanh -> xui -> chọn 1 hướng và đi 1 đoạn ngắn xem:
				- có đom đóm -> đi theo đom đóm tìm event -> áp dụng cách xác định vị trí theo event.
				- có event -> áp dụng cách xác định vị trí theo event.
				- có tường -> áp dụng cách xác định vị trí theo tường.
				- vẫn không có gì -> quay đầu chọn hướng khác vì khả năng lớn là cái hướng đó chả có cm gì cả.
		Ví dụ: spawn tại Y, đi dò sang bên phải ta tìm thấy event, vì ta đi từ bên trái qua nên có thể xác định ta đang ở vị trí C -> có 2 event khác ở gần hướng TB(A) và TN(D) so với điểm C.
				
				   
Tăng số lượng đom đóm nhận được, cách lấy point thì cũng không khó chắc ae cũng biết rồi.

	+ Lấy đủ Ascen 8 điểm sẽ tăng được tối thiểu 40% đom đóm cho ascen tương ứng, với tôi thì Maji chỉ cần Tincture nên tăng 60%.
	+ Khi đi nên di chuyển theo con đường đom đóm nếu có và cố gắng ăn event vì số lượng đom đóm event cho rất nhiều.
	+ Khi đi và xung quanh event thường có đom đóm rải thành vòng tròn bao quanh ta không cần lấy vội vì khi cố lấy nó sớm sẽ hao "Pin" làm ta không đi xa lấy event được, ta có thể quay lại lấy chúng sau khi hết "Pin".
	+ Lượng "Pin" ban đầu thường chỉ đủ cho 2 event, vậy nên nếu thấy bất kì điểm tiếp tế "Pin" nào thì đừng ngại mà chạy qua để lấy.
	+ Sau khi hết "Pin", quay lại và đi dọc theo mép các khu vực tối ban nãy ta bỏ qua để vét thêm 1 ít đom đóm còn thừa và quái ở gần nếu có.

Sau cùng thì nếu áp dụng đúng thì trung bình sẽ vét được khoảng từ 5-6k, xui thì 2-3k, hên thì tỉ lệ cook khá cao vì quái khỏe quá. (À nếu có thể nên vét đều 2-3 loại đom đóm, 1 loại loot có vẻ k ngon)
