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


## LiquidEffect
## Настройка бафов и дебафов жидкостей при употреблении.
```json
"LiquidEffect": [
       {
            "m_LiquidID": 67108864,
            "m_BaffOnlyText": [],
            "m_BaffForCountLiquid": 1000,
            "m_BaffPlayerStats": {},
            "m_BaffPlayerAgents": {
                "2": -400.0
            }
        },
        {
            "m_LiquidID": 524288,
            "m_BaffOnlyText": [],
            "m_BaffForCountLiquid": 1000,
            "m_BaffPlayerStats": {
                "Health": 20.0,
                "Blood": 1500.0
            },
            "m_BaffPlayerAgents": {
                "2": -800.0
            }
        },
]
```
- **`m_LiquidID`**: `int` ИД жидкости для которой эффект.
- **`m_BaffOnlyText`**: `string`  Временно не используется...
- **`m_BaffForCountLiquid`**: `int` Кол-во выпитой жидкости для которой будет действовать эффект. То есть параметры ниже будут разделены на это кол-во. Допустим вы настроили чтобы у вас добавлялось 100 ХП. 100ХП растянутся на употребление 1000 мл жидкости.
- **`m_BaffPlayerStats`**: `map<string, float>` Настройки для управления статусом персонажа. Blood, Health, Shock. А также кол-во увеличения или уменьшения при употреблении.
- **`m_BaffPlayerAgents`**: `map<int, float>` Настройки для управления агентами у персонажа. ID агента, а также увеличение его или уменьшения при употреблении.


## LiquidEffect
## Настройка отображения названия агентов в списке бафов и дебафов.
```json
"AgenstSettings": [
        {
            "agentsID": 1,
            "titleText": "#STR_RLF_Agents_CHOLERA"
        },
        {
            "agentsID": 2,
            "titleText": "#STR_RLF_Agents_INFLUENZA"
        }
]
```
- **`agentsID`**: `int` ИД агента.
- **`titleText`**: `string` название агента (холеры, сальмонеллы и т.п.)

