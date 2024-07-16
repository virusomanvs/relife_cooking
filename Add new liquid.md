## Добавление новой жидкости
Чтобы добавить новую жидкость, откройте файл relife_Cooking_Liquids/config.cpp и в конце найдите класс cfgLiquidDefinitions и добавьте туда вашу жидкость по примеру ниже
```c#
class cfgLiquidDefinitions
{
	class Liquid1 // Уникальное имя класса
	{
		type=5000; //Уникальный айди жидкости, не должен повторяться
		displayName="$STR_liq_LIQUID_WATER"; //Наименование жидкости
		name="$STR_liq_LIQUID_WATER"; //Наименование жидкости
		flammability=-10; //Горючесть, оставить как есть для кулинарии
		colorWidget = 0x0065FF27; //Цвет виджета при наведении на кастрюлю 
		class Nutrition
		{
			fullnessIndex=1;
			energy=100; //Кол-во добавляемой еды при при 100 мл жидкости.
			water=100; //Кол-во добавляемой воды при при 100 мл жидкости.
			nutritionalIndex=75;
			toxicity = 0;
			digestibility=2;
		};
	};
  class Liquid2 // Уникаль
	{
		type=5000;
		displayName="$STR_liq_LIQUID_WATER";
		name="$STR_liq_LIQUID_WATER";
		flammability=-10;
		colorWidget = 0x0065FF27;
		class Nutrition
		{
			fullnessIndex=1;
			energy=100;
			water=100;
			nutritionalIndex=75;
			toxicity = 0;
			digestibility=2;
		};
	};
};
```
После того как вы добавите жидкость сюда, вам нужно обозначить ее в емкостях, чтобы вы могли наливать ее в другие емкости. Для этого 
