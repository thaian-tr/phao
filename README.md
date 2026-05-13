# phao
CHƯƠNG 1 

1. Một số khái niệm và định nghĩa
- Theo ITU (International Telecommunication Union): "IoT là một cơ sở hạ tầng toàn cầu cho xã hội thông tin, cho phép các dịch vụ tiên tiến bằng cách liên kết các vật thể (vật lý hoặc ảo) dựa trên các công nghệ thông tin và truyền thông hiện có và tương lai."
- Theo IETF ((Internet Engineering Task Force): "IoT là một mạng lưới toàn cầu gồm các đối tượng được kết nối với nhau, có khả năng định danh duy nhất, dựa trên các giao thức truyền thông tiêu chuẩn."
- Theo IEEE (Institute of Electrical and Electronics Engineers): "IoT là một mạng lưới các đối tượng, mỗi đối tượng được nhúng cảm biến và kết nối với Internet."
- Theo WSIS 2005 (World Summit on the Information Society): "Bằng cách nhúng các thiết bị truyền tín hiệu di động tầm ngắn vào nhiều thiết bị và đồ vật hàng ngày, tạo ra các hình thức giao tiếp mới giữa con người và thiết bị, cũng như giữa các thiết bị với nhau."
- Theo Gartner: "IoT là mạng lưới các đối tượng vật lý có chứa công nghệ nhúng để tương tác với các trạng thái bên trong của chúng hoặc môi trường bên ngoài."
- Theo Kevin Ashton (Người đầu tiên giới thiệu thuật ngữ IoT): "IoT là khái niệm sử dụng cảm biến để kết nối thế giới vật lý với thế giới số, cho phép hệ thống máy tính hiểu và phản ứng với môi trường."
- Theo IoTAgenda: "IoT là một hệ thống các thiết bị máy tính, máy cơ khí và thiết bị số, các vật thể, động vật hoặc con người có liên quan với nhau được cung cấp mã định danh duy nhất (UID) và có khả năng truyền dữ liệu qua mạng mà không cần tương tác giữa con người với nhau hoặc giữa con người với máy tính."
- Theo Forbes: "IoT là một khái niệm kết nối bất kỳ thiết bị nào có công tắc bật/tắt với Internet (và/hoặc với nhau), từ điện thoại di động, máy pha cà phê, máy giặt, tai nghe, đèn, thiết bị đeo tay đến các thiết bị phức tạp hơn như động cơ phản lực hoặc giàn khoan dầu."
- Theo IoT Association: "IoT là mạng lưới các thiết bị vật lý được kết nối với Internet, cho phép thu thập và trao đổi dữ liệu mà không cần sự can thiệp của con người."
- Theo Cisco Systems: "IoT mô tả mạng lưới gồm hàng tỷ đối tượng vật lý trên thế giới, được kết nối với nhau thông qua Internet và có khả năng chia sẻ dữ liệu."

2. MỘT SỐ MỐC THỜI GIAN
- 1990: Máy nướng bánh mì được cho là đồ vật đầu tiên được kết nối internet.
- 1999: Thuật ngữ “internet of things” được đề xuất bởi Kevin Ashton khi thuyết trình về một hệ thống cảm biến và nhãn nhận dạng qua tần số radio (RFID) gắn trên hàng hóa để quản lý chuỗi cung ứng.
- 2000: LG giới thiệu chiếc tủ lạnh có kết nối internet đầu tiên trên thế giới
- 2008: Hội nghị quốc tế đầu tiên về IoT được tổ chức tại Zurich, Thụy Sĩ.
- 2009: Theo Cisco, đây là thời điểm mà mạng internet vạn vật thực sự được khai sinh, khi số lượng thiết bị được kết nối internet vượt dân số thế giới.
- 2012: Hội nghị Internet Châu Âu diễn ra với chủ đề “Internet of Things”.
- 2021: Ước tính có hơn 46 tỷ thiết bị được kết nối trên Internet.


CHƯƠNG 2
2.1. CẢM BIẾN VÀ CƠ CẤU CHẤP HÀNH
- Cảm biến (Sensor) IoT là thiết bị quan sát một hoặc nhiều thuộc tính của một thực thể vật lý và chuyển đổi các thuộc tính đó thành thông tin. Đầu ra của cảm biến có thể là tín hiệu tương tự (analog) hoặc là tín hiệu số
- Cơ cấu chấp hành (Actuator) (bộ truyền động) là thiết bị cóthể thay đổi một hoặc nhiều thuộc tính của một thực thể vật lý để đáp ứng với thông tin nhận được.

Các đại lượng cần đo (m) thường không có tính chất điện (như nhiệt độ, áp suất ...) tác động lên cảm biến cho ta một đặc trưng (s) mang tính chất điện (như điện tích, điện áp, dòng điện hoặc trở kháng) chứa đựng thông tin cho phép xác định giá trị của đại lượng đo. Đặc trưng (s) là hàm của đại lượng cần đo (m):
s = F(m)
- (s) là đại lượng đầu ra (hoặc là phản ứng của cảm biến)
- (m) là đại lượng đầu vào hay kích thích (có nguồn gốc là đại lượng cần đo).

2.2. Đường cong chuẩn của cảm biến
Khái niệm: Đường cong chuẩn cảm biến là đường cong biểu diễn sự phụ thuộc của đại lượng điện (s) ở đầu ra của cảm biến vào giá trị của đại lượng đo (m) ở đầu vào.

Phương pháp chuẩn cảm biến
+ Chuẩn đơn giản
Trong trường hợp đại lượng đo chỉ có một đại lượng vật lý duy nhất tác động lên một đại lượng đo xác định và cảm biến sử dụng không nhạy với tác động của các đại lượng ảnh hưởng, người ta dùng phương pháp chuẩn đơn giản. Thực chất của chuẩn đơn giản là đo các giá trị của đại lượng đầu ra ứng với các giá xác định không đổi của đại lượng đo ở đầu vào.
Việc chuẩn được tiến hành theo hai cách:
- Chuẩn trực tiếp: các giá trị khác nhau của đại lượng đo lấy từ các mẫu chuẩn hoặc các phần tử so sánh có giá trị biết trước với độ chính xác cao.
- Chuẩn gián tiếp: kết hợp cảm biến cần chuẩn với một cảm biến so sánh đã có sẵn đường cong chuẩn, cả hai được đặt trong cùng điều kiện làm việc. Khi tác động lên hai cảm biến với cùng một giá trị của đại lượng đo ta nhận được giá trị tương ứng của cảm biến so sánh và cảm biến cần chuẩn. Lặp lại tương tự với các giá trị khác của đại lượng đo cho phép ta xây dựng được đường cong chuẩn của cảm biến cần chuẩn.

+ Chuẩn nhiều lần
Khi cảm biến có phần tử bị trễ (trễ cơ hoặc trễ từ), giá trị đo được ở đầu ra phụ thuộc không những vào giá trị tức thời của đại lượng cần đo ở đầu vào mà còn phụ thuộc vào giá trị trước đó của của đại lượng này. Trong trường hợp như vậy, người ta áp dụng phương pháp chuẩn nhiều lần và tiến hành như sau:
- Đặt lại điểm 0 của cảm biến: đại lượng cần đo và đại lượng đầu ra có giá trị tương ứng với điểm gốc, m=0 và s=0.
- Đo giá trị đầu ra theo một loạt giá trị tăng dần đến giá trị cực đại của đại lượng đo ở đầu vào.
- Lặp lại quá trình đo với các giá trị giảm dần từ giá trị cực đại.
Khi chuẩn nhiều lần cho phép xác định đường cong chuẩn theo cả hai hướng đo tăng dần và đo giảm dần.

2.3. Các đặc trưng
- Độ nhạy của cảm biến: Mức độ thay đổi của tín hiệu đầu ra khi đại lượng đầu vào thay đổi. Độ nhạy cao giúp cảm biến phản ứng tốt với biến đổi nhỏ. (Sự thay đổi tối thiểu của thông số đo được gây ra thay đổi có thể phát hiện được trong tín hiệu đầu ra )
- Độ phân giải của cảm biến: Sự thay đổi tối thiểu trong hiện tượng mà cảm biến có thể phát hiện
- Độ tuyến tính của cảm biến: Mức độ mà đầu ra của cảm biến thay đổi tuyến tính theo đầu vào. Cảm biến tuyến tính dễ xử lý và hiệu chỉnh.
- Sai số và độ chính xác: Sai số là sự chênh lệch giữa giá trị đo được và giá trị thực của đại lượng cần đo. Độ chính xác phản ánh mức độ gần đúng của kết quả đo so với giá trị thực.
- Thời gian hồi đáp: Khoảng thời gian cảm biến cần để phản ứng với sự thay đổi của đại lượng đo và đạt đến giá trị ổn định.
- Vùng làm việc danh định: Khoảng giá trị của đại lượng đo mà cảm biến có thể hoạt động ổn định và chính xác.
- không gây nên hư hỏng: vùng gây thay đổi đặc trưng của cảm biến, mang tính thuận nghịch
- không phá huỷ: vùng gây thay đổi đặc trưng của cảm biến, ko thuận nghịch (cần chuẩn lại)

2.4. Nguyên lý chế tạo cảm biến
Các cảm biến được chế tạo dựa trên cơ sở các hiện tượng vật lý và được phân làm hai loại:
- Cảm biến tích cực: là các cảm biến hoạt động như một máy phát, đáp ứng (s) là điện tích, điện áp hay dòng.
- Cảm biến thụ động: là các cảm biến hoạt động như một trở kháng trong đó đáp ứng (s) là điện trở, độ tự cảm hoặc điện dung.

Các hiệu ứng:
- Hiệu ứng nhiệt điện
- Hiệu ứng hoả điện
- Hiệu ứng áp điện
- Hiệu ứng cảm ứng điện từ
- Hiệu ứng quang điện
- Hiệu ứng quang - điện - từ
- Hiệu ứng Hall

2.5. KHUẾCH ĐẠI, LỌC VÀ XỬ LÝ TÍN HIỆU
Lọc nhiễu cho tín hiệu cảm biến
- Khi tín hiệu bị nhiễu gây khó khăn trong việc điều khiển và giám sát.
- Sử dụng bộ lọc nhiễu để khắc phục các nhiễu trong tín hiệu analog, giúp hệ thống chạy ổn định, chính xác.
- Các tín hiệu truyền về theo chuẩn công nghiệp hiện nay chủ yếu là dùng tín hiệu 4-20mA.

2.6. Chuyển đổi ADC, DAC
Quá trình chuyển đổi ADC gồm ba bước chính: lấy mẫu, lượng tử hóa, mã hóa.

2.7. QUÁ TRÌNH XỬ LÝ DỮ LIỆU
1. Thu thập dữ liệu:
2. Lọc dữ liệu:
3. Biến đổi dữ liệu:
4. Tổ chức và lưu trữ:
5. Phân tích dữ liệu:
6. Trình bày kết quả:

2.5. CÁC GIẢI THUẬT XỬ LÝ DỮ LIỆU
Tiền xử lý dữ liệu cảm biến
- Lọc nhiễu (Noise Filtering): Sử dụng các bộ lọc để loại bỏ nhiễu khỏi dữ liệu cảm biến.
- Chuẩn hóa dữ liệu (Normalization): Đưa dữ liệu về cùng một thang đo để dễ phân tích.
- Phát hiện và xử lý dữ liệu thiếu (Missing Data Handling): Dùng kỹ thuật nội suy hoặc thay thế bằng giá trị trung bình hoặc Nhân tố ma trận xác suất (PMF) để xử lý dữ liệu khuyết thiếu.
- Xử lý dữ liệu ngoại lệ (Data Outlier Detection): Phát hiện và xử lý các giá trị cảm biến bất thường – những giá trị
khác biệt rõ rệt so với phần lớn dữ liệu còn lại.

Phân tích dữ liệu cảm biến
- Các giải thuật phân tích dữ liệu giúp hệ thống IoT hiểu, dự đoán và phản ứng với dữ liệu từ cảm biến. Bao gồm học máy, học sâu, thống kê, chuỗi thời gian và xử lý tại biên.
- Học máy: Sử dụng các thuật toán như Decision Tree, Random Forest,… phân loại trạng thái thiết bị hoặc dự đoán sự cố. Ví dụ: dự đoán lỗi động cơ từ dữ liệu cảm biến rung.
- Học sâu: Áp dụng CNN, RNN phân tích dữ liệu phức tạp như hình ảnh, chuỗi thời gian. Ví dụ: nhận dạng hình ảnh từ camera IoT hoặc phân tích nhịp tim từ cảm biến y tế.
- Phân tích thống kê và chuỗi thời gian
- Xử lý dữ liệu tại biên (Edge Analytics)

CHƯƠNG 3

I. IPv6 cho mạng IoT
Địa chỉ IPv6 có chiều dài 128bit với tổng không gian IPv6 là 2^128 địa chỉ
+ Các dạng địa chỉ IPv6
Địa chỉ IPv6 không còn duy trì khái niệm broadcast. Mọi chức năng của địa chỉ broadcast trong IPv4 được đảm nhiệm thay thế bởi địa chỉ IPv6 multicast. Theo cách thức gói tin được gửi đến đích, IPv6 bao gồm ba loại địa chỉ sau:
- Unicast: Địa chỉ unicast xác định một giao diện duy nhất. Địa chỉ unicast được sử dụng trong giao tiếp một – một
- Multicast: Địa chỉ multicast định danh một nhóm nhiều giao diện. Địa chỉ multicast được sử dụng trong giao tiếp một – nhiều.
- Anycast: Anycast là khái niệm mới của địa chỉ IPv6. Địa chỉ anycast cũng xác định tập hợp nhiều giao diện. Tuy nhiên, trong mô hình định tuyến, gói tin có địa chỉ đích anycast chỉ được gửi tới một giao diện duy nhất trong tập hợp. Giao diện đó là giao diện “gần nhất” theo khái niệm của thủ tục định tuyến.

Các lợi thế từ sự cải thiện thiết kế của IPv6 phù hợp với IoT 
Các lợi ích và ưu điểm của IPv6 cho IoT có thể được liệt kê như sau: 
• Khả năng mở rộng 
IPv6 cung cấp không gian địa chỉ khổng lồ với 2128 (3,4×1038) địa chỉ, đủ để giải quyết nhu cầu của bất kỳ thiết bị giao tiếp hiện tại và tương lai. 
 • Giải quyết rào cản NAT 
Nhiều ứng dụng IoT không chấp nhận NAT, vì yêu cầu địa chỉ có khả năng truy cập toàn cầu. IPv6 không cần thiết phải dùng NAT.
• Cải thiện về định tuyến 
IPv6 cung cấp kết nối end-to-end, với cơ chế định tuyến hiệu quả hơn, giảm kích thước và độ phức tạp của bảng định tuyến. IPv6 cho phép các nhà cung cấp dịch vụ Internet (ISP) tổ hợp các tiền tố trong mạng của khách hàng của họ thành một tiền tố duy nhất và quảng bá chỉ một tiền tố này trên IPv6.
• Tự động cấu hình địa chỉ không trạng thái Stateless (SLAAC) 
IPv6 cung cấp cơ chế tự cấu hình địa chỉ (cơ chế không trạng thái). Điều này cho phép cấu hình plug-and-play, không cần tới cấu hình nhân công hay thông qua sự phân phối IP bằng máy chủ DHCP. Tính năng này rất hữu ích trong mạng IoT.
• Multicast và Anycast 
Sử dụng multicast trong IPv6 hạn chế rủi ro hơn trong IPv4 rất nhiều nhờ vào cách tạo địa chỉ cho các nhóm điểm đến. IP multicast đặc biệt hữu ích trong các mạng IoT quy mô lớn.
Anycast không được thiết kế trong IPv4. Trong IPv6, anycast cho phép xác minh tính sẵn sàng của thiết bị trong mạng. Anycast rất hữu ích trong mạng cục bộ và mạng cảm biến. Nó có thể được sử dụng cho các kho lưu trữ tài nguyên IoT, các máy chủ bảo mật và các cổng kết nối đa hướng.
• Chất lượng dịch vụ 
Cấu trúc địa chỉ IPv6 cung cấp một số bit để xác định mức Chất lượng dịch vụ (QoS) trong xử lý các gói tin. Ví dụ: IPv6 có thể sử dụng các tính năng QoS như Diffserv hoặc IntServ để ưu tiên các cảnh báo cảm biến khẩn cấp. Tính năng này đã được khai thác thực tế trên các bộ định tuyến thương mại khi chúng đã được cấu hình để sử dụng các bit này trong địa chỉ IPv6. 
• Tính di động 
IPv6 cung cấp các tính năng và giải pháp mạnh mẽ để hỗ trợ tính di động của cả hai nút cuối, và các nút định tuyến. IPv4 cũng cung cấp tính di động nhưng giao thức Internet di động (MIP) mà IPv4 sử dụng rất không hiệu quả: mỗi gói phải đi qua Home Agent bằng đường dẫn hình tam giác. Trong IPv6, một phiên bản mới của MIP là MIPv6 đã được phát triển. So với MIP, MIPv6 giảm độ trễ chuyển giao nhờ một số tối ưu hóa trong các cơ chế: phát hiện chuyển động (MD); phát hiện địa chỉ trùng lặp (DAD) và Cập nhật ràng buộc (BU). 
• Bảo mật 
Thiết kế của IPv4 không tính đến vấn đề bảo mật. Do đó, bảo mật trong IPv4 phải được thực hiện bằng các ứng dụng. Để khắc phục hạn chế này, tính năng bảo mật được thiết kế trong IPv6, có thể kể tới gồm: (i) IPSec: IPv6 được thiết kế cho kết nối đầu cuối – đầu cuối; (ii) Bắt buộc sử dụng IPsec cho IPv6 di động để đảm bảo khả năng định tuyến trở lại; (iii) Không gian địa chỉ lớn; (iv) Thủ tục Neighbor Discovery.
• Phiên bản IPv6 có sẵn cho các thiết bị tiêu thụ điện năng thấp 
Việc sử dụng IPv6 cho các ứng dụng IoT đã được nghiên cứu trong nhiều năm. Một trong những kết quả đáng kể là phiên bản nén của IPv6 cho thiết bị công suất thấp, cụ thể là IPv6 qua Mạng cá nhân không dây công suất thấp (6LoWPAN). Đây là một cơ chế đơn giản và hiệu quả cho phép rút ngắn kích thước địa chỉ IPv6 cho các thiết bị có hạn chế, đồng thời cho phép bộ định tuyến biên dịch các địa chỉ nén thành địa chỉ IPv6 thông thường.

II. Định tuyến trong mạng tổn hao năng lượng thấp (Low-power Lossy Networks - LLN)
+ Mạng tổn hao năng lượng thấp (LLN): Mạng tổn hao năng lượng thấp (LLN) là một mạng bao gồm một hoặc nhiều bộ định tuyến và những thiết bị nhúng bị giới hạn điện năng nhận vào, giới hạn bộ nhớ và tài nguyên xử lý. LLN tối ưu nhất khi sử dụng trong những trường hợp tiết kiệm năng lượng

+ Giao thức định tuyến trong mạng tổn hao năng lượng thấp (RPL)
RPL là giao thức định tuyến cho các mạng tổn hao năng lượng thấp nói chung và mạng cảm biến không dây nói riêng. Các mạng có đặc điểm: 1. Tiêu thụ năng lượng thấp, 2.Có khả năng mất mát dữ liệu cao, 3.Gồm nhiều thiết bị cảm biến, thường dùng trong môi trường IoT.
RPL sử dụng các DAG trong mạng để định tuyến. 
- DAG ROOT: nút có chức năng tập trung và xử lý dữ liệu từ các nút khác trong mạng gửi đến. Mọi tuyến liên kết trong DAG đều hướng về và kết thúc tại DAG ROOT.
- DAG rank: thông số cho biết vị trí tương đối của nút so với DAG ROOT. Những nút có rank càng lớn càng xa DAG ROOT. DAG ROOT luôn có rank bằng 1.
- DAG parent: Trong cùng một DAG, nút A được gọi là nút cha (parent) của nút B khi A và B có kết nối trực tiếp với nhau và A có rank nhỏ hơn B. Khi đó, nút B được gọi là nút con (children) của nút A.
- DAG sibling: nút A là ngang cấp (sibling) với nút B trong một DAG nếu chúng có cùng rank trong DAG đó.

Cấu trúc DODAG: Mỗi nút trong mạng xây dựng một cây định tuyến hướng về một đích (thường là bộ thu dữ liệu hoặc gateway).
Hỗ trợ nhiều loại lưu lượng:
- Upward traffic: từ thiết bị đến root.
- Downward traffic: từ root đến thiết bị.
- Point-to-point traffic: giữa các thiết bị trong mạng.

+ RPL Instance (Thực thể RPL): một tập hợp các cấu hình định tuyến riêng biệt trong một mạng RPL.
Mỗi instance có thể có:
- Mục tiêu định tuyến khác nhau: ví dụ tối ưu hóa độ trễ, tiết kiệm năng lượng, độ tin cậy…
- Các tham số hoạt động riêng biệt: như metric, mode of operation, các chính sách định tuyến.
- Một DODAG hoặc nhiều DODAGs: là cấu trúc cây định tuyến hướng về một hoặc nhiều nút root.

Một số đặc điểm chính của RPL Instance:
- Instance ID: Mỗi instance được định danh bằng một mã số duy nhất gọi là Instance ID.
- Phân biệt traffic: Cho phép các loại traffic khác nhau (ví dụ: dữ liệu cảm biến, điều khiển, cảnh báo…) sử dụng các đường định tuyến tối ưu riêng.
- Quản lý linh hoạt: Một thiết bị có thể tham gia vào nhiều RPL Instance cùng lúc nếu cần thiết.

+ CÁC LOẠI BẢN TIN ĐIỀU KHIỂN TRONG DAG: 1.DAG Information Soliciation (DIS), 2.DAG Information Object (DIO), 3.Destination Advertisement Object (DAO)

+ ĐẶC ĐIỂM CỦA RPL
- Tối ưu hóa năng lượng: RPL sử dụng các thuật toán định tuyến giúp giảm tiêu thụ năng lượng và kéo dài tuổi thọ thiết bị.
- Khả năng phục hồi: Có thể tự động tái cấu trúc cây định tuyến khi có nút bị lỗi hoặc thay đổi vị trí.
- Sử dụng các hàm mục tiêu (Objective Function): Dựa vào độ tin cậy, độ trễ, năng lượng còn lại để chọn tuyến đường tốt nhất.

+ Hàm mục tiêu
- Hàm OF0 tìm quãng đường ngắn nhất đến nút gốc root. OF0 đánh dấu các nút gần root nhất, đặt thứ tự ưu tiên. Từ đó, chọn ra các nút cha có thứ tự ưu tiên cao nhất. Sử dụng metric là số lượng bước nhảy (hop count).
- Hàm MRHOF sử dụng ETX (Expected Transmission Count – số lần truyền dự kiến) làm metric chính để đánh giá chất lượng tuyến đường. Các bước hoạt động:

III. KIẾN TRÚC IoT
3.2. Mô hình tham chiếu 3 lớp
Lớp 1: Lớp thiết bị
Lớp này bao gồm các cảm biến, thiết bị chấp hành và các bộ điều khiển như vi xử lý/vi điều khiển, PLC, FPGA đến các máy tính nhúng.
Lớp thiết bị thực hiện đo lường và thu thập dữ liệu các đại lượng vật lý thông qua các cảm biến, điều khiển các thiết bị chấp hành và có thể truyền và nhận dữ liệu từ các thiết bị khác qua mạng.
Lớp 2: Lớp mạng
Chức năng lớp mạng xác định các giao thức truyền thông khác nhau được sử dụng cho việc kết nối mạng và thực hiện điện toán biên.
Lớp mạng bao gồm các thiết bị liên kết mạng như Hub, Switch, Router; các thiết bị chuyển đổi giao thức mạng như Gateways; đến các thiết bị có khả năng lưu trữ, xử lý cục bộ trước khi gửi dữ liệu lên Server trung tâm.
Lớp 3: Lớp ứng dụng
Đây là trung tâm lưu trữ dữ liệu hay đám mây điện tử.
Lớp này thực hiện thu nhận dữ liệu từ lớp mạng, lưu trữ, xử lý dữ liệu và ra quyết định dựa trên các thuật toán AI/ML hoặc các công cụ phân tích dữ liệu hiện đại.

3.3. Mô hình tham chiếu IoT 5 lớp	
Lớp 1: Lớp đối tượng (Objects Layer)
Cảm biến/Thiết bị là thành phần quan trọng giúp thu thập dữ liệu trực tiếp từ môi trường xung quanh. Tất cả dữ liệu này có thể có nhiều mức độ phức tạp khác nhau. Nó có thể là một cảm biến theo dõi nhiệt độ đơn giản, hoặc nó có thể ở dạng nguồn cấp dữ liệu video.
Lớp 2: Lớp trừu tượng đối tượng (Object Abstraction Layer)
Tất cả dữ liệu thu thập được sẽ được gửi đến cơ sở hạ tầng đám mây. Các cảm biến phải được kết nối với đám mây bằng nhiều phương tiện khác nhau
Lớp 3: Lớp quản lý dịch vụ (Service Management Layer)
	Lớp Quản lý dịch vụ hoặc Middleware (ghép nối) kết hợp dịch vụ với người yêu cầu dựa trên địa chỉ và tên. Lớp này cho phép các lập trình viên ứng dụng IoT làm việc với các đối tượng không đồng nhất mà không cần xem xét đến một nền tảng phần cứng cụ thể.
Lớp 4: Lớp ứng dụng (Application Layer)
	Lớp ứng dụng cung cấp các dịch vụ theo yêu cầu của khách hàng.(Ví dụ, lớp ứng dụng có thể cung cấp các phép đo nhiệt độ và độ ẩm không khí cho khách hàng yêu cầu dữ liệu đó.)
Lớp 5: Lớp quản lý (business layer)
	Lớp quản lý quản lý các hoạt động và dịch vụ hệ thống IoT tổng thể. Trách nhiệm của lớp này là xây dựng mô hình kinh doanh, đồ thị, lưu đồ, v.v. dựa trên dữ liệu nhận được từ lớp Ứng dụng.

3.4. Mô hình tham chiếu IoT 7 lớp
Thiết bị, kết nối, điện toán biên, tích lũy dữ liệu, trừu tượng hóa, ứng dụng, hợp tác & quy trình.

IV. CÁC THÀNH PHẦN CỦA IoT
B. Giao thức ứng dụng
- Giao thức CoAP (Constrained Application Protocol):Giao thức ứng dụng dùng cho thiết bị IoT có tài nguyên hạn chế, hoạt động qua UDP để tiết kiệm năng lượng.
- Giao thức MQTT (Message Queuing Telemetry Transport): Giao thức nhắn tin sử dụng mô hình xuất bản/đăng ký, phù hợp với mạng băng thông thấp và thiết bị hạn chế tài nguyên.
- Giao thức XMPP (Extensible Messaging and Presence Protocol): Giao thức nhắn tin tức thời dựa trên XML, hỗ trợ xác thực, mã hóa và tương thích cao, có thể dùng trong IoT.

C. Các giao thức cơ sở hạ tầng
1. RPL – Routing Protocol for Low Power and Lossy Network: giao thức định tuyến cho mạng tổn hao năng lượng thấp nói chung và mạng cảm biến không dây nói riêng:

2. 6LowPAN: Low power Wireless Personal Area Networks (WPAN) đây là khu vực mạng cá nhân không dây công suất thấp) mà nhiều IoT có thể giao tiếp dựa vào có một số đặc điểm đặc biệt khác với các công nghệ lớp liên kết trước đây như kích thước gói giới hạn (ví dụ: tối đa 127 byte cho IEEE 802.15.4), độ dài địa chỉ khác nhau và băng thông thấp

Theo sau 6LoWPAN , biểu đồ dữ liệu được bao bọc bởi bởi sự kết hợp của một số tiêu đề. Các tiêu đề này có bốn loại được xác định bằng 2 bit :
- (00) NO 6LoWPAN Header: các gói không phù hợp với đặc điểm kỹ thuật 6LoWPAN sẽ bị loại bỏ.
- (01) Dispatch Header: Nén tiêu đề IPv6 hoặc đa hướng
- (10) Mesh Addressing: xác định các gói IEEE 802.15.4 phải được chuyển tiếp đến trình liên kết.
- (11) Fragmentation: dùng đối với các biểu đồ dữ liệu có độ dài vượt quá một khung IEEE 802.15.4
Phân tích hiệu suất của 6LoWPAN trong mạng cảm biến không dây cho thấy độ trễ có tăng lên. Một số vấn đề khác như: tỷ lệ mất gói dữ liệu cao, dễ bị can thiệp

3. IEEE 802.15.4: giao thức IEEE 802.15.4 được tạo ra để chỉ định lớp con trong Kiểm soát truy cập trung bình (MAC) và lớp vật lý (PHY) cho mạng vùng riêng không dây tốc độ thấp (LR-WPAN). Nó cung cấp một giao tiếp đáng tin cậy, khả năng hoạt động trên các nền tảng khác nhau và có thể xử lý một số lượng lớn các nút (khoảng 65k). Nó cũng cung cấp các dịch vụ bảo mật, mã hóa và xác thực ở mức độ cao. Tuy nhiên, nó không cung cấp đảm bảo QoS.

IEEE 802.15.4 hỗ trợ ba băng tần kênh tần số và sử dụng phương pháp trải phổ chuỗi trực tiếp (DSSS).
Dựa trên các kênh tần số đã sử dụng, lớp vật lý truyền và nhận dữ liệu trên ba tốc độ dữ liệu:
- 250 kbps ở 2,4 GHz
- 40 kbps ở 915 MHz
- 20 kbps ở 868 MHz.
Tần số cao và dải tần số rộng => thông lượng cao và độ trễ thấp
Tần số thấp => độ nhạy tốt hơn và bao phủ khoảng cách lớn hơn.

Chuẩn IEEE 802.15.4 hỗ trợ hai loại nút mạng:
- Full Function Device(FFD) thiết bị đầy đủ chức năng hoạt động như một bộ điều phối mạng khu vực cá nhân (PAN) hoặc chỉ như một nút bình thường.
- Reduced Function Device(RFD): thiết bị chức năng giảm là các nút rất đơn giản với tài nguyên bị hạn chế. Chúng chỉ có thể giao tiếp với một điều phối viên và bị giới hạn trong cấu trúc liên kết hình sao.
+ Tiêu chuẩn của các cấu trúc liên kết để tạo thành mạng IEEE 802.15.4 là hình sao, peer-to-peer (mesh), và cluster-tree.

4. Bluetooth Low Energy(BLE): bluetooth năng lượng thấp hoặc bluetooth thông minh sử dụng radio tầm ngắn với lượng điện năng tối thiểu để hoạt động trong thời gian dài hơn (thậm chí trong nhiều năm) so với các phiên bản trước của nó.
Ưu điển: phạm vi phủ sóng (khoảng 100 mét) gấp mười lần so với Bluetooth cổ điển trong khi độ trễ của nó thấp hơn 15 lần và có thể hoạt động nhờ công suất truyền từ 0,01 mW đến 10 mW.

Điện năng tiêu thụ của BLE thấp hơn IEEE 802.15.4, IEEE 802.11ah có khả năng truyền dữ liệu tốt hơn IEEE 802.15.4 kể cả khi ở trạng thái có tải và không tải. Tuy nhiên IEEE 802.15.4 lại tiết kiệm năng lượng hơn, đặc biệt trong các mạng lưới lớn.

5. EPCglobal: The Electronic Product Code(EPC) mã sản phẩm điện tử là một số nhận dạng duy nhất được lưu trữ trên thẻ RFID và được sử dụng cơ bản trong quản lý chuỗi cung ứng để xác định các mặt hàng.
EPC được phân thành bốn loại: 96-bit, 64-bit (I), 64-bit (II) và 64-bit (III). Tất cả các loại EPC 64-bit hỗ trợ khoảng 16 000 công ty có danh tính riêng và bao gồm từ 1 đến 9 triệu loại sản phẩm và 33 triệu số sê-ri cho mỗi loại. Loại 96-bit hỗ trợ khoảng 268 triệu công ty có danh tính riêng, 16 triệu loại sản phẩm và 68 tỷ số sê-ri cho mỗi loại

Hệ thống RFID chia thành 2 phần chính:
- radio signal transponder (tag) bộ phát đáp tín hiệu vô tuyến
- tag reader (bộ đọc thẻ).
Qua một số bài nghiên cứu cho thấy giao thức EPC Gen-2 tốt hơn CDMA

6. LTE-A ((Long Term Evolution—Advanced )(Tiến hóa dài hạn — Nâng cao): LTE-A bao gồm một tập hợp các giao thức truyền thông di động phù hợp tốt cho cơ sở hạ tầng Truyền thông kiểu máy (MTC) và IoT, đặc biệt là cho các thành phố thông minh nơi mong đợi độ bền lâu dài của cơ sở hạ tầng. Hơn nữa, nó vượt trội hơn các giải pháp di động khác về chi phí dịch vụ và khả năng mở rộng.

Kiến trúc của mạng LTE-A dựa trên 2 phần chủ yếu
- Đầu tiên là Mạng lõi (Core Network - CN): kiểm soát các thiết bị di động và xử lý các luồng gói IP.
- Phần khác là mạng truy cập vô tuyến (RAN): xử lý truyền thông không dây và truy cập vô tuyến, đồng thời thiết lập các giao thức mặt phẳng người dùng và mặt phẳng điều khiển.
RAN và CN được kết nối thông qua giao diện S1. Các thiết bị di động hoặc MTC có thể kết nối với các trạm gốc trực tiếp hoặc thông qua cổng MTC (MTCG). Tuy nhiên, giao thức này có những thách thức như tắc nghẽn mạng cao khi một số lượng lớn thiết bị đang truy cập mạng. Một thách thức khác, QoS có thể bị xâm phạm khi thiết bị MTC cố gắng truy cập mạng thông qua lựa chọn eNB hoặc MTCG.

7. Z-Wave
 Z-Wave như một giao thức truyền thông không dây công suất thấp cho mạng tự động hóa gia đình - Home Automation Networks (HAN), nó đã được sử dụng rộng rãi trong các ứng dụng điều khiển từ xa trong nhà thông minh cũng như các tên miền thương mại cỡ nhỏ.
- Z-Wave cho phép kết nối điểm-điểm khoảng 30 mét, dùng cho các ứng dụng cần truyền dữ liệu nhỏ (ví dụ truyền tìn hiệu giữa các thiết bị thông minh trong nhà, cho phép chúng có thể “nói chuyện” với nhau)
- Z-Wave hoạt động ở bằng tần ISM (khoảng 900MHz) và cho phép truyền đi với tốc độ 40kbps, và lên tới 200kbps.
- Z-Wave có cấu trúc lưới. Các thiết bị (nút) được liên kết với 1 trung tâm. Qua đó sẽ dễ dàng điều khiển bằng điện thoại/ máy tính
- Đánh giá: Nhược điểm: cấu trúc khép kín, không tương thích được với nhiều thiết bị, bị phụ thuộc vào đường truyền wifi, giá thành vẫn cao. Ưu điểm: độ tin cậy, khả năng mở rộng, hiệu suất mạnh.

CHƯƠNG 4

1. Một chương trình cơ bản gồm hai phần chính: setup() và loop()
- setup() là nơi khai báo các giá trị biến, khai báo thư viện, thiết đặt thông số...Chạy một lần duy nhất sau khi cấp nguồn cho arduino, cho đến khi reset lại hệ thống.
- loop() sẽ khởi động sau khi khi setup() chạy xong, đây là nơi các chương trình được lặp đi lặp lại cho đến khi dừng cấp nguồn hoặc reset lại hệ thống.

2. Hằng số và biến số
- HIGH: là một hằng số có giá trị nguyên là 1. Trong điện tử, HIGH là một mức điện áp lớn hơn 0V (Giá trị của HIGH được định nghĩa khác nhau trong các mạch điện khác nhau, nhưng thường được quy ước ở các mức như 3,3V; 5V;...)
- LOW: là một hằng số có giá trị nguyên là 0. Trong điện tử, LOW là mức điện áp 0V.
- INPUT
- INPUT_PULLUP
- OUTPUT

3. Hàm và thủ tục
Digital I/O
- pinMode()
- digitalWrite() 
- digitalRead()
Analog I/O
- analogReference()
- analogRead()
- analogWrite()
