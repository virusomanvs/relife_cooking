## Настройка рецептов RecipeList
## RecipeList
```json
"RecipeList": [
       {
            "recipeUniqueID": 3,
            "m_NeedLiquid": 512,
            "m_Ingredients": [
                [
                    "Rice",
                    "Rice_OtherType"
                ],
                [
                    "SheepSteakMeat"
                ]
            ],
            "m_IngredientsCount": [
                1,
                3
            ],
            "m_TimeToCooking": 350.0,
            "m_ResultLiquid": 4194304,
            "m_ResultLiquidQuantity": 2000,
            "recipeName": "#STR_liq_LIQUID_RICESOUP"
        }
]
```
- **`recipeUniqueID`**: `int` Уникальный ID рецепта. Не должен повторятся.
- **`m_NeedLiquid`**: `string`  Необходимая жидкость для приготовления. 512 - Вода. Можете указать любую другую, чтобы делать цепочки супов.
- **`m_Ingredients`**: `array <array<string>>` Массив с ингредиентами. Как в примере выше, блюдо может быть приготовлено из двух видов риса, и оба можно указать в массиве. То есть с такой настройкой как выше, блюдо можно будет приготовить, из одного любого вида риса, и 3 кусков баранины.
- **`m_IngredientsCount`**: `int` Количество предметов для каждого массива. Кол-во элементов в массиве должно быть столько же сколько и элементов в ингредиентах.
- **`m_TimeToCooking`**: `float` Время приготовления в секундах если готовится из полного состояния ингредиентов. Если допустим положить в кастрюлю по 50% ингредиентов, то время готовки будет зависит от этого.
- **`m_ResultLiquid`**:  `int` ID жидкости в результате успешного приготовления.
- **`m_ResultLiquidQuantity`**:  `int` Кол-во. жидкости после приготовления при полном кол-ве ингредиентов. Если допустим положить в кастрюлю по 50% ингредиентов, то количество жидкости будет зависит от этого.
- **`recipeName`**:  `string` Название рецепта в меню.
  