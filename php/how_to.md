# with を使って関係フィールド取得時のフラット化

関係テーブルが増えてしまうと、select と join を書くのが結構ややこしくなってしまいます。

Laravel Eloquent では with を使って、モデルで定義された関係を用いて外部テーブルのデータを取り出すことができる

<pre>
// App/Models/Item.php
    public function unit()
    {
        return $this->belongsTo(Unit::class, 'unit_id');
    }
// App/Models/Unit.php
    public function items()
    {
        return $this->hasMany(Item::class, 'unit_id');
    }
    
// コントローラでwith('relation:id,field1,field2,...')で使う
Item::with('unit:id,code')->get(['name','unit_id']);
</pre>
