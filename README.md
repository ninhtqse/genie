# Genie English

[![Latest Version](https://img.shields.io/github/release/esbenp/genie.svg?style=flat-square)](https://github.com/esbenp/genie/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Build Status](https://img.shields.io/travis/esbenp/genie/master.svg?style=flat-square)](https://travis-ci.org/esbenp/genie)
[![Coverage Status](https://img.shields.io/coveralls/esbenp/genie.svg?style=flat-square)](https://coveralls.io/github/esbenp/genie)
[![Total Downloads](https://img.shields.io/packagist/dt/optimus/genie.svg?style=flat-square)](https://packagist.org/packages/optimus/genie)

## Introduction

A base repository class for Eloquent with convenience methods that cover most queries. Useful to abstract away
your persistence layer from your business code.

**Dedicated to Genie**

Dedicated to the World's best (and only) Genie in a bottle. [Congrats on the freedom my man](https://www.youtube.com/watch?v=SUfP6IGQD00).

## Installation

```bash
composer require ninhtqse/genie
```

## Implementation

The examples will use a hypothetical Eloquent model named `User`.

```
<?php

namespace App\Repositories;

use App\Models\User;
use Ninhtqse\Genie\Repository;

class UserRepository extends Repository
{
    protected function getModel()
    {
        return new User;
    }
}
```

## Options

Genie is already integrated with [Ninhtqse\Bruno](https://github.com/esbenp/bruno).
See Bruno documentation for more information.
The `$options` key given by all get-methods takes the following format:

Parameter | Value type | Description
--------- | ---------- | -----------
includes | array | Array of relationships to eager load
sort | array | Array of sorting rules, e.g. `[['key' => 'username', 'direction' => 'ASC']]`
filter_groups | array | See Bruno documentation
limit | int | Rows per page
page | int | The page to start from (use with limit)
fields | array | Get the fields according to the parameters passed.
skip | integer | The starting position is in the database
take | integer | Number of records taken

*Note:* If you use the controller of Bruno it will automatically parse the request's
query string into the correct format.

## API

The examples will use a hypothetical Eloquent model named `User`.

### get (array $options = [])

Get all `User` rows

### getById ($id, array $options = [])

Get one `User` by primary key

### getRecent (array $options = [])

Get `User` rows ordered by `created_at` descending

### getRecentWhere (string $column, mixed $value, array $options = [])

Get `User` rows where `$column=$value`, ordered by `created_at` descending

### getWhere (string $column, mixed $value, array $options = [])

Get `User` rows where `$column=$value`

### getWhereArray (array $clauses, array $options = [])

Get `User` rows by multiple where clauses (`[$column1 => $value1, $column2 => $value2]`)

### getWhereIn (string $column, array $values, array $options = [])

Get `User` rows where `$column` can be any of the values given by `$values`

### getLatest (array $options = [])

Get the most recent `User`

### getLatestWhere (string $column, mixed $value, array $options = [])

Get the most recent `User` where `$column=$value`

### delete ($id)

Delete `User` rows by primary key

### deleteWhere ($column, $value)

Delete `User` rows where `$column=$value`

### deleteWhereArray (array $clauses)

Delete `User` rows by multiple where clauses (`[$column1 => $value1, $column2 => $value2]`)

## Standards

This package is compliant with [PSR-1], [PSR-2] and [PSR-4]. If you notice compliance oversights,
please send a patch via pull request.

[PSR-1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[PSR-2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[PSR-4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md

## Contributing

Please see [CONTRIBUTING](https://github.com/esbenp/genie/blob/master/CONTRIBUTING.md) for details.

## License

The MIT License (MIT). Please see [License File](https://github.com/esbenp/genie/blob/master/LICENSE) for more information.

------------------------------------------------------------------------------------------------------------------------------------------------

# Genie VIETNAM

[![Latest Version](https://img.shields.io/github/release/esbenp/genie.svg?style=flat-square)](https://github.com/esbenp/genie/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Build Status](https://img.shields.io/travis/esbenp/genie/master.svg?style=flat-square)](https://travis-ci.org/esbenp/genie)
[![Coverage Status](https://img.shields.io/coveralls/esbenp/genie.svg?style=flat-square)](https://coveralls.io/github/esbenp/genie)
[![Total Downloads](https://img.shields.io/packagist/dt/optimus/genie.svg?style=flat-square)](https://packagist.org/packages/optimus/genie)

## Giới thiệu

Một lớp kho lưu trữ cơ sở cho Eloquent với các phương thức tiện lợi bao gồm hầu hết các truy vấn. Hữu ích để tóm tắt
lớp bền vững của bạn từ mã doanh nghiệp của bạn.

**Dành riêng cho Genie**

Dành riêng cho Thần đèn [Chúc mừng sự tự do](https://www.youtube.com/watch?v=SUfP6IGQD00).

## Cài đặt

```bash
composer require ninhtqse/genie
```

## Thực hiện

Các ví dụ sẽ sử dụng Eloquent model giả định có tên là `User`.

```
<?php

namespace App\Repositories;

use App\Models\User;
use Ninhtqse\Genie\Repository;

class UserRepository extends Repository
{
    protected function getModel()
    {
        return new User;
    }
}
```

## Tùy chọn

Genie đã được tích hợp với [Ninhtqse\Bruno](https://github.com/ninhtqse/bruno).
Xem tài liệu để biết thêm thông tin.
Biến `$options` được cung cấp bởi tất cả các phương thức get có định dạng sau:

Parameter | Kiểu dữ liệu | Mô tả
--------- | ---------- | -----------
includes | array | Mảng các mối quan hệ để tải eager load
sort | array | Mảng các quy tắc sắp xếp, e.g. `[['key' => 'username', 'direction' => 'ASC']]`
filter_groups | array | Xem tài liệu Bruno
limit | int | Hàng trên mỗi trang
page | int | Trang để bắt đầu (sử dụng có giới hạn)
fields | array | Nhận các trường theo các tham số được truyền vào.
skip | integer | Vị trí bắt đầu nằm trong cơ sở dữ liệu
take | integer | Số lượng bản ghi muốn lấy

*Lưu ý:* Nếu bạn sử dụng bộ điều khiển của Bruno, nó sẽ tự động phân tích cú pháp của yêu cầu
chuỗi truy vấn thành định dạng chính xác.

## API

Các ví dụ sẽ sử dụng một giả thuyết Eloquent model tên `User`.

### get (array $options = [])

lấy ra tất cả bản ghi `User`

### getById ($id, array $options = [])

Lấy ra 1 bản ghi của `User` theo khóa chính

### getRecent (array $options = [])

Lấy bản ghi của `User` sắp xếp theo `created_at` giảm dần

### getRecentWhere (string $column, mixed $value, array $options = [])

Lấy ra bản ghi của `User` theo điều kiện `$column=$value`, sắp xếp `created_at` giảm dần

### getWhere (string $column, mixed $value, array $options = [])

Lấy ra bản ghi của `User` theo điều kiện `$column=$value`

### getWhereArray (array $clauses, array $options = [])

Lấy ra bản ghi của `User` theo một bảng các điều kiện được truyền vào (`[$column1 => $value1, $column2 => $value2]`)

### getWhereIn (string $column, array $values, array $options = [])

Lấy ra bản ghi của `User` theo giá trị `$column` có thể nằm trong mảng `$values`

### getLatest (array $options = [])

Lấy ra bản ghi của `User` được thêm vào gần đây nhất

### getLatestWhere (string $column, mixed $value, array $options = [])

Lấy ra bản ghi của `User` được thêm vào gần đây nhất và theo điều kiện `$column=$value`

### delete ($id)

Xóa bản ghi của `User` theo khóa chính

### deleteWhere ($column, $value)

Xóa bản ghi của `User` theo điều kiện `$column=$value`

### deleteWhereArray (array $clauses)

Xóa bản ghi của `User` theo một mảng các điều kiện được truyền vào (`[$column1 => $value1, $column2 => $value2]`)

## Tiêu chuẩn

Gói này tuân thủ [PSR-1], [PSR-2] và [PSR-4]. Nếu bạn nhận thấy giám sát tuân thủ,
xin vui lòng gửi một bản vá thông qua yêu cầu kéo.

[PSR-1]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md
[PSR-2]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md
[PSR-4]: https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md


## Giấy phép

Giấy phép MIT (MIT). Mời các bạn xem [Giấy phép đăng ký](https://github.com/ninhtqse/genie/blob/master/LICENSE) để biết thêm thông tin.
