# phao
I
1. Các lĩnh vực chức năng của quản trị mạng (Theo mô hình ISO) Công tác quản trị mạng được chia thành 5 lĩnh vực chức năng chính: 
•	Quản lý lỗi (Fault Management): Đây là lĩnh vực phức tạp nhất, có nhiệm vụ phát hiện, ghi nhận, thông báo và tự động khắc phục lỗi để duy trì hiệu quả hoạt động của mạng. 
•	Quản lý cấu hình (Configuration Management): Theo dõi và thu thập thông tin cấu hình hệ thống (phần cứng, phần mềm) và lưu trữ vào cơ sở dữ liệu để phân tích. 
•	Quản lý kiểm toán/kế toán (Accounting Management): Đo lường việc sử dụng tài nguyên, phân tích mẫu sử dụng và thiết lập hạn ngạch cho người dùng để khai thác hệ thống hiệu quả nhất. 
•	Quản lý hiệu năng (Performance Management): Đo lường và quản lý băng thông, thời gian hồi đáp để duy trì hiệu năng mạng ở mức có thể truy cập được. 
•	Quản lý an ninh (Security Management): Điều khiển truy cập tài nguyên dựa trên đặc quyền để bảo vệ các dữ liệu nhạy cảm khỏi người dùng không được phép. 

2. Kiến trúc hệ thống quản trị mạng và Kỹ thuật giám sát
•	Kiến trúc: Bao gồm Thực thể quản trị (trạm quản lý trung tâm - NMS) và Thực thể bị quản trị (các thiết bị mạng chứa Agent và cơ sở dữ liệu quản lý). 
•	Phương thức Poll (Get): Trạm quản lý (Manager) chủ động hỏi thông tin định kỳ từ thiết bị (Device). Cách này giúp lấy đúng thông tin cần thiết nhưng có thể cập nhật chậm hoặc bỏ sót sự kiện nếu chu kỳ hỏi dài. 
•	Phương thức Alert (Trap): Thiết bị tự động gửi thông báo cho Manager ngay khi có sự kiện/biến cố xảy ra. Cách này giúp cập nhật tức thời, nhưng nếu đường truyền gián đoạn thì Manager sẽ không nhận được cảnh báo. 

3. Giao thức quản trị mạng đơn giản (SNMP)
•	SNMP được dùng để quản lý các thiết bị mạng chạy trên nền TCP/IP, hoạt động trên giao thức UDP (Port 161 cho Polling và Port 162 cho Trapping). 
•	Thành phần dữ liệu: Các thông tin của thiết bị được gọi là đối tượng (Object) và được nhận dạng bằng mã số OID (Object ID). Tập hợp các đối tượng này tạo thành cơ sở thông tin quản trị MIB (Management Information Base). 
•	Các bản tin phương thức hoạt động:
  o	GetRequest / GetNextRequest: Manager yêu cầu Agent cung cấp thông tin của đối tượng (dựa vào OID) hoặc đối tượng kế tiếp trong cây MIB. 
  o	SetRequest: Manager yêu cầu thiết lập lại giá trị cho một đối tượng trên Agent (đối tượng phải có quyền READ_WRITE). 
  o	GetResponse: Agent gửi trả lời cho Manager khi nhận được các bản tin Get hoặc Set. 
  o	Trap: Agent chủ động gửi cảnh báo (có thể là generic trap hoặc specific trap) cho Manager khi có sự kiện bất thường xảy ra. 
•	Cơ chế bảo mật của SNMP:
  o	Community string: Đóng vai trò như "mật khẩu" giao tiếp giữa Manager và Agent (gồm Read, Write và Trap community). 
  o	View: Giới hạn quyền, chỉ cho phép đọc một phần cụ thể của cây MIB tương ứng với community string. 
  o	SNMP Access Control List (ACL): Thiết lập danh sách các địa chỉ IP của Manager được phép truy cập và quản lý Agent. 

II
2.1. Bộ định tuyến (Router)
•	Chức năng chính: Hoạt động ở tầng mạng (tầng 3 mô hình OSI), có nhiệm vụ kết nối nhiều mạng khác nhau (LAN, MAN, WAN) và tìm đường đi tối ưu (định tuyến) để chuyển tiếp các gói tin dựa vào địa chỉ IP. 
•	Chức năng khác: Kiểm soát tắc nghẽn, đảm bảo chất lượng dịch vụ (QoS), phân mảnh/ghép dữ liệu, quản lý địa chỉ (NAT, DHCP), tích hợp tường lửa và quản trị mạng. 
•	Thành phần cấu tạo:
  o	Bên trong: CPU, ROM (chứa trình kiểm tra POST, Bootstrap, Mini-IOS), RAM/DRAM (lưu bảng định tuyến, file cấu hình đang chạy running-config), Flash (lưu hệ điều hành Cisco IOS) và NVRAM (lưu file cấu hình khởi động startup-config). 
  o	Bên ngoài (Cổng giao tiếp): Các cổng mạng LAN (FastEthernet, GigabitEthernet), cổng WAN (Serial) và cổng quản trị (Console, AUX). 
•	Hệ điều hành Cisco IOS: Cung cấp dịch vụ định tuyến, chuyển mạch và bảo mật; quá trình khởi động gồm kiểm tra phần cứng, tải IOS từ Flash và tải cấu hình từ NVRAM. 

2.2. Các giao thức định tuyến
•	Khái niệm: Là ngôn ngữ giao tiếp cho phép các router chia sẻ thông tin về mạng lưới để tự động xây dựng và duy trì "bảng định tuyến" (Routing table). 
•	Phân loại định tuyến:
  o	Định tuyến tĩnh (Static Routing): Cấu hình thủ công bởi người quản trị, dùng cho mạng nhỏ và đường đi không thay đổi. 
  o	Định tuyến động (Dynamic Routing): Router tự động cập nhật và tìm đường đi (VD: RIP, OSPF, EIGRP, BGP), sử dụng cho mạng lớn. 
•	Các tiêu chí chọn đường:
  o	Khoảng cách quản trị (AD - Administrative Distance): Đánh giá độ tin cậy của thông tin định tuyến (giá trị từ 0 - 255, càng nhỏ càng đáng tin cậy). 
  o	Metric: Giá trị định lượng mức độ tối ưu của đường đi (đường có metric nhỏ nhất sẽ được chọn). RIP dùng số bước nhảy (hop-count), OSPF dùng băng thông, EIGRP dùng nhiều thông số (băng thông, độ trễ, tải...). 
•	Giao thức định tuyến cần đáp ứng việc hội tụ mạng (convergence) nhanh chóng và hỗ trợ cân bằng tải (load balancing). 

2.3. Phần mềm mô phỏng PacketTracer
•	Chức năng: Là phần mềm giả lập hệ thống mạng trực quan của Cisco, giúp mô phỏng gần như chính xác các thiết bị mạng thực tế và các giao thức đi kèm. 
•	Cách sử dụng: Cung cấp giao diện để người dùng chọn thiết bị (Router, Switch, Hub, PC, Laptop...), kết nối cáp (cáp thẳng, cáp chéo, cáp console), cấu hình IP và kiểm tra kết nối mạng. 
•	Kiểm tra mô phỏng: Sử dụng công cụ (như Add Simple PDU) để xem mô phỏng quá trình gửi và nhận gói tin (như ICMP, ARP) theo thời gian thực (Simulation mode). 
•	Phần mềm cho phép lưu lại (.pkt) và mở các sơ đồ mạng đã thiết kế. 

2.4. Cấu hình và quản trị Router
•	Giao diện dòng lệnh (CLI): Cấu trúc phân cấp với các chế độ quản trị chính:
  o	User EXEC Mode (>): Chỉ xem thông tin cơ bản. 
  o	Privileged EXEC Mode (#): Thực thi mọi lệnh xem cấu hình và trạng thái bằng lệnh enable. 
  o	Global Configuration Mode ((config)#): Chế độ cấu hình toàn cục bằng lệnh configure terminal. 
  o	Interface Config/Line Config: Chế độ cấu hình chi tiết cho từng cổng kết nối hoặc đường line. 
•	Các lệnh cấu hình cơ bản: Đặt tên hostname, cài đặt mật khẩu mã hóa/không mã hóa (enable password, enable secret, password console/vty), cấp IP cho cổng giao tiếp, và lưu cấu hình (copy running-config startup-config). 
•	Lệnh kiểm tra (Show): show running-config, show interfaces, show ip interface brief, show ip route (xem bảng định tuyến), v.v. 
•	Cấu hình định tuyến: Bao gồm cú pháp để cấu hình đường đi tĩnh (ip route) hoặc khởi tạo quá trình định tuyến động (router rip hoặc router ospf) và khai báo mạng (network). 

2.5. Cấu hình và quản trị Switch
•	Cấu hình cơ bản: Sử dụng CLI tương tự như Router để đặt tên, thiết lập mật khẩu truy cập và lưu file cấu hình. 
•	Cài đặt VLAN: Tạo mạng LAN ảo (VLAN) bằng cách khai báo ID/Tên VLAN và gán các cổng của switch vào VLAN đó (switchport access vlan). 
•	VLAN-Trunking (VTP): Chỉ định chế độ VTP (Server/Client) và cấu hình cổng Trunk (switchport mode trunk) để chuyển tiếp dữ liệu của nhiều VLAN trên cùng một đường dây. 
•	VLAN-Routing: Sử dụng Switch Layer 3 (với lệnh ip routing) hoặc Router (cấu hình Subinterface, hay còn gọi là Router-on-a-stick) để định tuyến và kết nối các VLAN khác nhau lại với nhau.

III
3.1. Giới thiệu Windows Server
•	Windows Server là hệ điều hành dành cho Server, chuyên cung cấp các dịch vụ mạng và hoạt động trong môi trường Domain. 
•	Mô hình Workgroup (Peer-to-peer): Các máy tính có vai trò ngang nhau, dữ liệu và tài nguyên được quản lý phân tán tại máy cục bộ (thông tin người dùng lưu trong file SAM mã hóa). Mô hình này chỉ phù hợp với mạng nhỏ (dưới 10 máy) và yêu cầu bảo mật không cao. 
•	Mô hình Domain (Client-server): Quản lý tập trung thông qua ít nhất một máy điều khiển miền (Domain Controller - DC). Thông tin người dùng được quản lý bởi dịch vụ Active Directory (lưu trong file NTDS.DIT), giúp việc chứng thực và quản lý tài nguyên được tập trung, phù hợp với các công ty vừa và lớn. 
•	Một số thuật ngữ: Stand-alone là máy chủ không tham gia domain; Member Server là máy chủ tham gia domain nhưng không đóng vai trò Domain Controller. 

3.2. Quản trị Active Directory
•	Khái niệm: Active Directory (AD) là dịch vụ thư mục độc quyền của Microsoft giúp quản trị tập trung tất cả các đối tượng trong vùng (người dùng, máy tính, thiết bị...). AD mang lại nhiều ưu điểm như: quản lý tập trung, bảo mật dữ liệu, áp dụng chính sách nhóm (Group Policy), khả năng mở rộng và ủy quyền quản trị. 
•	Thành phần (Directory Services): Gồm có Objects (đối tượng như user, máy in, server), Attribute (thuộc tính mô tả đối tượng), Schema (định nghĩa các đối tượng và thuộc tính) và Container (vật chứa nhiều object bên trong). 
•	Kiến trúc logic: Bao gồm Domain (nơi lưu trữ các object), OU - Organizational Unit (đơn vị tổ chức nhỏ nhất để ủy quyền quản trị), Tree (tập hợp nhiều domain theo cấu trúc hình cây mẹ-con) và Forest (tập hợp nhiều domain/tree có mối quan hệ tin cậy chia sẻ chung schema và global catalog). 
•	Kiến trúc vật lý: Bao gồm Site (đại diện cho vị trí địa lý của các domain) và Domain Controller (máy chủ chứa bản sao AD, làm nhiệm vụ xác thực người dùng). 
•	Hệ thống có thể triển khai thêm các DC đồng hành (ADC) để dự phòng cho DC chính (PDC), hoặc triển khai máy chủ dạng Read-Only Domain Controller (RODC) tại các vị trí không đảm bảo an toàn vật lý. 

3.3. Quản lý tài khoản người dùng và nhóm
•	Tài khoản người dùng (User Account): Dùng để đăng nhập, xác thực, cấp quyền và theo dõi (auditing) việc truy cập tài nguyên. Có hai loại: 
  o	Local user account: Tạo và lưu trữ trên máy cục bộ (file SAM), chỉ được truy cập tài nguyên cục bộ. 
  o	Domain user account: Tạo trên Domain Controller, cho phép người dùng đăng nhập và truy cập tài nguyên trên toàn hệ thống mạng. 
•	Yêu cầu tài khoản: Tên đăng nhập dài từ 1-20 ký tự, không chứa các ký tự cấm đặc biệt. Mật khẩu phải dài tối thiểu 6 ký tự và có độ phức tạp (kết hợp chữ hoa, chữ thường, số và ký tự đặc biệt). 
•	Tài khoản nhóm (Group Account): Là đối tượng đại diện cho một nhóm người dùng, giúp quản trị viên gán quyền hàng loạt một cách dễ dàng. Nhóm không được phép đăng nhập hệ thống. 
•	Phân loại nhóm: Có 2 kiểu nhóm là Security Group (liên quan đến an ninh, gán quyền, có mã SID) và Distribution Group (danh sách phân phối email, không có SID, không dùng gán quyền). 
•	Phạm vi nhóm: Gồm 4 loại là Local, Global, Domain Local và Universal, tuân theo các quy tắc lồng nhóm (Nesting) và các chiến lược triển khai quyền như AGDLP.

IV
4.1. Các khái niệm cơ bản về bảo mật mạng
•	Bảo mật mạng là gì: Là việc bảo vệ dữ liệu an toàn trên môi trường trực tuyến. Theo Liên minh Viễn thông Quốc tế (ITU), đây là tập hợp các công cụ, chính sách, phương pháp quản lý rủi ro và công nghệ dùng để bảo vệ hệ thống mạng và tài sản. 
•	Các yếu tố đảm bảo an toàn thông tin:
  o	Tính bí mật: Đảm bảo thông tin chỉ được sử dụng đúng đối tượng. 
  o	Tính toàn vẹn: Thông tin đầy đủ và nguyên vẹn về cấu trúc. 
  o	Tính sẵn sàng: Thông tin luôn tiếp cận được để phục vụ đúng mục đích. 
  o	Tính chính xác: Dữ liệu phải đáng tin cậy và chính xác. 
  o	Tính không khước từ: Có thể kiểm chứng được nguồn gốc hoặc người đưa tin. 
•	Các khái niệm về rủi ro:
  o	Mối đe dọa (Threat): Các hành động/sự kiện có khả năng xâm hại đến hệ thống. Bao gồm mục tiêu tấn công (dịch vụ, tính toàn vẹn), đối tượng tấn công (hacker) và hành vi tấn công (nghe lén, ăn cắp). 
  o	Lỗ hổng hệ thống (Vulnerability): Điểm yếu mà kẻ tấn công có thể khai thác, tồn tại trong lập trình (back-door), hệ điều hành, ứng dụng, vật lý hoặc thủ tục quản lý. 
  o	Nguy cơ hệ thống (Risk): Được hình thành từ sự kết hợp giữa mối đe dọa và lỗ hổng hệ thống (Nguy cơ = Mối đe dọa + Lỗ hổng). 

4.2. Một số nguy cơ tấn công
•	Tấn công quét mạng (Scanning Attacks):
  o	Port Scanning: Gửi thông điệp để xác định các cổng đang mở nhằm biết dịch vụ nào đang chạy (ví dụ dùng Nmap). 
  o	Vulnerability Scanning: Quét để xác định lỗ hổng bảo mật, bản cập nhật bị thiếu trên hệ thống. 
  o	Network Scanning (Ping Sweep): Xác định các máy đang hoạt động trên hệ thống mạng. 
•	Tấn công giả mạo địa chỉ IP (Spoofing Attacks): Kẻ tấn công giả mạo địa chỉ IP để hạn chế bị phát hiện, qua mặt hệ thống tường lửa và IDS. 
•	Tấn công chiếm quyền máy chủ (Session Hijacking): Hacker đánh cắp cookie sau khi người dùng đã xác thực với máy chủ, ngắt kết nối của nạn nhân và chiếm lấy phiên làm việc đó. Quá trình gồm dò tìm session, tái đồng bộ kết nối và chèn các gói tin tấn công. 
•	Tấn công từ chối dịch vụ (DoS - Denial of Service): Làm hệ thống quá tải khiến máy chủ bị tê liệt, không thể đáp ứng yêu cầu hợp lệ. Các công cụ phổ biến gồm Ping of Death, LAND Attack, WinNuke, CPU Hog. 
•	Tấn công từ chối dịch vụ phân tán (DDoS): Là hình thức DoS nhưng được tiến hành từ nhiều máy tính khác nhau (mạng botnet). Cấu trúc gồm Master (máy điều khiển), Slave/Zombie (máy bị lây nhiễm) và Victim (mục tiêu). 
•	Tấn công cổng sau (Backdoor Attacks): Cài đặt chương trình ẩn giúp hacker xâm nhập lại dễ dàng và xóa dấu vết. Chúng thường được đặt tên giống các dịch vụ hệ thống Windows để ngụy trang. 

4.3. Một số giải pháp bảo mật mạng
Tài liệu tập trung vào hai giải pháp chính: IDS và Tường lửa (Firewall). 
4.3.1. Hệ thống phát hiện xâm nhập (IDS - Intrusion Detection System)
•	Chức năng: Giám sát lưu lượng mạng, phát hiện các hoạt động khả nghi và cảnh báo cho nhà quản trị. IDS phân tích sự kiện dựa trên dấu hiệu (signature) hoặc sự bất thường (anomaly). 
•	Phân loại:
  o	NIDS (Network Base IDS): Đặt ở các điểm kết nối mạng để giám sát toàn bộ lưu lượng. Ưu điểm là "trong suốt", quản lý được nhiều máy , nhưng không phân tích được dữ liệu mã hóa và có thể báo động giả. 
  o	HIDS (Host Base IDS): Cài đặt phần mềm trên một máy chủ (host) cụ thể để giám sát file log, CPU, Registry. Nó có thể phân tích dữ liệu mã hóa , nhưng sẽ mất tác dụng nếu hệ điều hành của host đó bị sập. 
4.3.2. Hệ thống tường lửa (Firewall)
•	Khái niệm: Là rào chắn (phần cứng hoặc phần mềm) giữa mạng an toàn và không an toàn. Firewall điều khiển truy cập bằng cách cho phép hoặc từ chối dữ liệu ra/vào dựa trên một tập luật (chính sách). 
•	Các vùng mạng cơ bản (Network Zones):
  o	Mạng nội bộ (LAN): Chứa các máy trạm, thiết bị mạng nội bộ. 
  o	Vùng DMZ: Vùng trung lập chứa các dịch vụ công khai ra Internet (Web, Mail, DNS Server). 
  o	Vùng Server Farm: Đặt các máy chủ không trực tiếp giao tiếp với Internet (như Database). 
•	Chính sách tường lửa: Mỗi luật (rule) thường gồm 7 thuộc tính: Chiều của gói tin, Giao thức, IP nguồn, Cổng nguồn, IP đích, Cổng đích, và Hành động (chấp nhận/từ chối)
