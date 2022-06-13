PORT 3000
{{domain}}=https://localhost:3000/api/v1/
quanLyNguoiDungRouter/
// đăng kí tài khoản
quanLyNguoiDungRouter.post('/dangKy'

https://localhost:3000/api/v1//quanLyNguoiDung/dangKy
// đăng nhập
quanLyNguoiDungRouter.post('/dangNhap',

https://localhost:3000/api/v1/quanLyNguoiDung/dangNhap
//lấy danh sách người dùng
quanLyNguoiDungRouter.get('/danhSachNguoiDung'

https://localhost:3000/api/v1/quanLyNguoiDung/danhSachNguoiDung/
//lấy thông tin người dùng theo id
quanLyNguoiDungRouter.get('/layThongTinNguoiDung?'

https://localhost:3000/api/v1/quanLyNguoiDung/layThongTinNguoiDung?id=1
// upload avata
quanLyNguoiDungRouter.post('/avatar',authenticate,uploadAvatar(),

https://localhost:3000/api/v1/quanLyNguoiDung/avatar
//lấy danh sách người dùng phân trang
quanLyNguoiDungRouter.get('/danhSachNguoiDung/:page/:pageSize' 

https://localhost:3000/api/v1/quanLyNguoiDung/danhSachNguoiDung/1/4
//tìm kiếm người dùng
quanLyNguoiDungRouter.get('/timNguoiDung?'

https://localhost:3000/api/v1/quanLyNguoiDung/timNguoiDung?tukhoa=ly
//tìm kiếm người dùng phân trang
quanLyNguoiDungRouter.get('/timNguoiDungPhanTrang?'

https://localhost:3000/api/v1/quanLyNguoiDung/timNguoiDungPhanTrang?tukhoa=nguyen&page=1&pageSize=3
//lấy thông tin tài khoản
quanLyNguoiDungRouter.get('/layThongTinCaNhan' ,authenticate,

{{domain}}/quanLyNguoiDung/layThongTinCaNhan
//lấy danh sách người dùng theo loại người dùng
quanLyNguoiDungRouter.get('/loaiNguoiDung?' ,[authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1/quanLyNguoiDung/loaiNguoiDung?role=ADMIN
//cập nhật thông tin người dùng
quanLyNguoiDungRouter.put('/' ,authenticate,

https://localhost:3000/api/v1/quanLyNguoiDung/
// thêm người dùng
quanLyNguoiDungRouter.post('/' ,[authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1//quanLyNguoiDung/
// xóa người dùng
quanLyNguoiDungRouter.delete('/:id',[authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1/quanLyNguoiDung/

+ quanLyPhimRouter
// lay danh sach phim
quanLyPhimRouter.get('/'

https://localhost:3000/api/v1/quanLyphim/
// lay danh sach phim phan trang
quanLyPhimRouter.get('/:page/:pageSize'

https://localhost:3000/api/v1/quanLyphim/2/5
// lay danh sach phim theo ngay phan trang
quanLyPhimRouter.get('/layDanhSachPhimTheoNgay?'

https://localhost:3000/api/v1/quanLyphim/layDanhSachPhimTheoNgay?page=1&pageSize=5
// them phim
 quanLyPhimRouter.post('/',[authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1/quanLyphim/
// xoa phim
 quanLyPhimRouter.delete('/:id' ,[authenticate,checkRole('ADMIN')]

https://localhost:3000/api/v1/quanLyphim/12
// lay phim theo id
quanLyPhimRouter.get('/:id',

https://localhost:3000/api/v1/quanLyphim/11
// cap nhat phim
quanLyPhimRouter.put('/:id', [authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1/quanLyphim/11
// them poster phim
quanLyPhimRouter.post('/poster', uploadPoster(),[authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1/quanLyphim/poster
// them phim upload poster
quanLyPhimRouter.post('/themPhimUploadPoster', uploadPoster(),[authenticate,checkRole('ADMIN')]

https://localhost:3000/api/v1/quanLyphim/themPhimUploadPoster
// update phim upLoad poster
 quanLyPhimRouter.put('/poster/:id', uploadPoster(),[authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1/quanLyphim/Poster/11

+ quanLyRapRouter
// lay danh sach he thong rap
quanLyRapRouter.get('/',

https://localhost:3000/api/v1/quanLyRap/
// lay thong tin he thong rap theo id
quanLyRapRouter.get('/:id',

https://localhost:3000/api/v1/quanLyRap/1
// lay danh sach phong & cum rap theo id he thong rạp
quanLyRapRouter.get('/layThongTinCumRap/:id',

https://localhost:3000/api/v1/quanLyRap/layThongTinCumRap/2
// lay thong tin rap theo mã rạp
quanLyRapRouter.get('/layThongTinPhongTheoRap/:id',

https://localhost:3000/api/v1/quanLyRap/layThongTinPhongTheoRap/5
// lay thong tin lich chieu theo id he thong rap
quanLyRapRouter.get('/lichChieuHeThong/:id',

https://localhost:3000/api/v1/quanLyRap/lichChieuHeThong/1
// lay thong tin lich chieu theo id phim
quanLyRapRouter.get('/lichChieuPhim/:id',

https://localhost:3000/api/v1/quanLyRap/lichChieuPhim/1

+quanLyDatVeRouter
//-- them lich chieu phim
quanLyDatVeRouter.post('/',[authenticate,checkRole('ADMIN')],

https://localhost:3000/api/v1/quanLyDatVe/
//--- lay lich chieu phim theo id lich chieu
quanLyDatVeRouter.get('/lichChieuPhim/:id',

https://localhost:3000/api/v1/quanLyDatVe/lichChieuPhim/3
// dat ve phim
quanLyDatVeRouter.post('/datVe/',[authenticate,checkRole('USER')],

https://localhost:3000/api/v1/quanLyDatVe/datVe/
// lay thong tin ve da dat theo id nguoi dung
quanLyDatVeRouter.get('/lichSuDatVe/',[authenticate,checkRole('USER')],
https://localhost:3000/api/v1/quanLyDatVe/lichSuDatVe/


