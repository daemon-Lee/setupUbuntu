1. Cài đặt ibus-unikey

Mở Terminal, thực hiện command sau để cài đặt ibus-unikey

    $ sudo apt-get install ibus-unikey

2. Khởi động lại phần mềm ibus

Để khởi động lại ibus, các bạn dùng command sau:

    $ ibus restart

3. Thiết lập gõ tiếng việt cho ibus trên Ubuntu 18.04

Bước 1: Tìm kiếm chức năng quản lý [ Settings ]

Bước 2: Ở cửa sổ [ Settings ] -> [ Region  & Language ] -> [Input Sources ] -> Bấm [ + ] để thêm 1 input source

Bước 3: Ở cửa sổ [ Add an Inpupt Source ] -> Tìm kiếm ngôn ngữ là “Vietnamese (Unikey)” -> Bấm “Add”

Bước 4: Sau đó restart lại Ubuntu và xác nhận Ibus-Unikey đã có 2 ngôn ngữ là tiếng Anh và tiếng Việt

Bạn có thể chuyển đổi qua lại giữa 2 ngôn ngữ bằng phìm tắt là “Windows + Space”
4. Thiết lập gõ tiếng việt cho ibus trên Ubuntu 16.04 và 17.10 (Version cũ)

Bước 1: Mở Terminal lên và chạy command sau để thiết lập gõ tiếng Việt cho Ibus

    $ ibus-setup

Bước 2: Cửa sổ [IBus Preferences] hiện ra.

Ở tab [ General ] -> Tích vào ô “Show icon on system tray”

Bước 3: Chuyển sang tab [ Input Method ] -> bấm vào “Add” để thêm ngôn ngữ tiếng Việt

Bước 4: Tìm kiếm ngôn ngữ “Vietnamese” -> Chọn “Unikey” -> Bấm “Add” để thêm ngôn ngữ tiếng Việt

