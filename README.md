# الكود الأول: حساب الطلب على الطاقة في فرنسا

# 1. الطلب على الطاقة في فرنسا (2000)
def demand_france_2000(demand_2015, growth_rate, years):
    """
    حساب الطلب على الطاقة في فرنسا لعام 2000 باستخدام معادلة النمو المركب.
    """
    return demand_2015 / (1 + growth_rate) ** years

# 2. معدل النمو بين 2015 و2016 في فرنسا
def growth_rate_france_2015_2016(demand_2015, demand_2016):
    """
    حساب معدل النمو بين 2015 و2016 في فرنسا.
    """
    return (demand_2016 - demand_2015) / demand_2015 * 100

# 3. استهلاك الطاقة الأولي في ألمانيا (2015)
def energy_demand_germany_2015(demand_2016, growth_rate_gdp, elasticity):
    """
    حساب استهلاك الطاقة الأولي في ألمانيا لعام 2015 باستخدام نمو الناتج المحلي الإجمالي.
    """
    return demand_2016 / (1 + growth_rate_gdp * elasticity)

# 4. التوقعات للطاقة الأولية في الأردن (2010-2017)
def predict_energy_demand_jor(years, initial_demand, growth_rate):
    """
    توقعات استهلاك الطاقة الأولية في الأردن من 2010 إلى 2017 باستخدام طريقة الانحدار الخطي.
    """
    predictions = []
    for year in years:
        demand = initial_demand * (1 + growth_rate) ** (year - years[0])
        predictions.append((year, demand))
    return predictions


# المعطيات

# بيانات فرنسا
demand_france_2015 = 5720  # Mtoe
growth_rate_france = 0.036  # 3.6% سنويًا
years_france = 15  # من 2000 إلى 2015
demand_france_2016 = 5970  # Mtoe

# بيانات ألمانيا
demand_germany_2016 = 1300  # Mtoe
gdp_growth_germany = 0.0652  # 6.52% نمو الناتج المحلي الإجمالي
elasticity = 2.4  # مرونة الطلب على الطاقة

# بيانات الأردن
years_jor = list(range(2010, 2018))  # من 2010 إلى 2017
initial_demand_jor = 6200  # Mtoe لعام 2010
growth_rate_jor = 0.06  # نمو سنوي مقدر بـ 6%

# حساب النتائج

# 1. حساب الطلب على الطاقة في فرنسا لعام 2000
demand_france_2000_value = demand_france_2000(demand_france_2015, growth_rate_france, years_france)
print(f"الطلب على الطاقة في فرنسا عام 2000: {demand_france_2000_value:.2f} Mtoe")

# 2. حساب معدل النمو بين 2015 و2016 في فرنسا
growth_rate_france_value = growth_rate_france_2015_2016(demand_france_2015, demand_france_2016)
print(f"معدل النمو بين 2015 و2016 في فرنسا: {growth_rate_france_value:.2f}%")

# 3. حساب استهلاك الطاقة الأولي في ألمانيا لعام 2015
demand_germany_2015_value = energy_demand_germany_2015(demand_germany_2016, gdp_growth_germany, elasticity)
print(f"استهلاك الطاقة الأولي في ألمانيا عام 2015: {demand_germany_2015_value:.2f} Mtoe")

# 4. حساب التوقعات للطاقة الأولية في الأردن (2010-2017)
predictions_jor = predict_energy_demand_jor(years_jor, initial_demand_jor, growth_rate_jor)
for year, demand in predictions_jor:
    print(f"توقعات استهلاك الطاقة في الأردن لعام {year}: {demand:.2f} Mtoe")
