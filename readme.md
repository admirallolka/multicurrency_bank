### multicurrency_bank


```php
<?php 
use MultiCurrency\Bank\Invoice;
use MultiCurrency\Bank\Currencies\Rub;
use MultiCurrency\Bank\Currencies\Usd;
use MultiCurrency\Bank\Currencies\Eur;
?>

<?php
$invoice = new Invoice([
    'currencies' => [
        'default' => Rub::class,
        'courses' => [
            [
                'from' => Eur::class,
                'to' => Rub::class,
                'course' => 80              
            ],
            [
                'from' => Usd::class,
                'to' => Rub::class,
                'course' => 70              
            ],
            [
                'from' => Eur::class,
                'to' => Usd::class,
                'course' => 1,      
            ],
        ], 
        'list' => [
            Rub::class,
            Usd::class,
            Eur::class
        ]    
    ],
])

?>
```
