
# Samples you need to try


## The simplest product management

```xml

<root org="doublechain"
    chinese_name="Simple PIM"
    english_name="Product Information Management"
>


    <platform
        name="PIM"
        founded="now()"
        contact_number="992887654321"
    />
    
   
    
</root>


```


## Adding Brand 

* Adding under platform, brand will be a list of platform, brand list, means platform has brand list


```xml

<root org="doublechain"
    chinese_name="Simple PIM"
    english_name="Product Information Management"
>


    <platform
        name="PIM"
        founded="now()"
        contact_number="992887654321"
    />
    <brand name="brand"  platform="platform()"/>
   
    
</root>
  
```

## Adding Product 

* under brand, product can be added, and it is also visible to platform
* We added a snack.jpg as snack image, this will be regard as a picture

```xml

<root org="doublechain"
    chinese_name="Simple PIM"
    english_name="Product Information Management"
>


    <platform
        name="PIM"
        founded="now()"
        contact_number="992887654321"
    />
    <brand name="Candys|Sees"  platform="platform()"/>
    <product name="popcorn|chocolate" image="snack.jpg" brand="brand()"  platform="platform()"/>
    
</root>
  
```

## Adding SKU

* under product, SKU can be added, also need to be visible to brand, platform
* a field called create_time with type createTime() added, this field can be maintained automatically

```xml
<root org="doublechain"
    chinese_name="Simple PIM"
    english_name="Product Information Management"
>
    <platform
        name="PIM"
        founded="now()"
        contact_number="992887654321"
    />
    <brand name="Candys|Sees"  platform="platform()"/>
    <product name="popcorn|chocklate" image="snack.jpg" brand="brand()"  platform="platform()"/>
    <sku name="sku" product="product()" brand="brand()" platform="platform()" create_time="createTime()"/>
</root>
 

```

## Have fun!

