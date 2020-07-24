## Access Control

<b>Access Control</b>, yaitu pengaturan untuk siapa saja yang bisa mengakses suatu halaman web. Pada materi ini kita akan memberikan akses kepada user yang sudah login untuk melakukan penambahan dan modifikasi Area. 

Apabila user belum login, maka tidak bisa melakukan hal tersebut.

1. Buka file `AreaController.php` yang berada di folder `/advanced/frontend/controllers` dan lakukan modifikasi pada public function behaviors. Dokumentasi bisa dilihat disini, [dokumentasi access control Yii2.](https://www.yiiframework.com/doc/api/2.0/yii-filters-accesscontrol)

```
public function behaviors()
    {
        return [
            'access'=> [
                'class'=>AccessControl::className(),
                'only'=>['create','update'],
                'rules'=>[
                    [
                        'allow'=>true,
                        'roles'=>['@'],
                    ],
                ],
            ],
            'verbs' => [
                'class' => VerbFilter::className(),
                'actions' => [
                    'delete' => ['POST'],
                ],
            ],
        ];
    }
```

2. Tambahkan `filter AccessControl` pada `use`. seperti berikut ini
```
use yii\filters\AccessControl;
```

3. Akses halaman area dengan link seperti berikut `http://localhost/advanced/frontend/web/index.php?r=area` lalu klik button create atau update, 
maka sebelum anda masuk kedalam form `create` ataupun `update` maka, `access control` akan bekerja dan menghantarkan kedalam form `login` terlebih dahulu. 

