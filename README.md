def nhap_kho_thuc_an_nhanh():
    danh_sach_mon_an = []

    while True:
        ten_mon = input("Nhập tên món ăn (nhập 'exit' để thoát): ")
        if ten_mon.lower() == "exit":
            break

        so_luong = input("Nhập số lượng: ")
        while not so_luong.isdigit():
            so_luong = input("Vui lòng nhập số nguyên cho số lượng: ")
        so_luong = int(so_luong)

        gia = input("Nhập giá món ăn: ")
        while True:
            try:
                gia = float(gia)
                break
            except ValueError:
                gia = input("Vui lòng nhập giá trị số cho giá món ăn: ")

        danh_sach_mon_an.append({
            "ten_mon": ten_mon,
            "so_luong": so_luong,
            "gia": gia
        })

    print("\n=== DANH SÁCH MÓN ĂN NHANH TRONG KHO ===")
    for mon in danh_sach_mon_an:
        print(f"- Tên món: {mon['ten_mon']}, Số lượng: {mon['so_luong']}, Giá: {mon['gia']}")
    print("=========================================")


if __name__ == "__main__":
    nhap_kho_thuc_an_nhanh()
