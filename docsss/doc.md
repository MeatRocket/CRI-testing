# Cloud Geography


### Summary<a name="Describtion"></a>
A .Net client to retrieve Countries, Languages, and Currencies information.The .Net client is built on .Net Standard so it supports Windows, Windows Store, Windows Phone, Mono, and Xamarin, also it has implemented an integrated caching so developers don't have to. Backend API is deployed on Microsoft Azure latest technology services. .Net client and backend API are both built using best practices as lead developers would expect.

### Installation<a name="Installation"></a>

------------

#### Package Manager<a name="Package Manager"></a>

```batch
Install-Package AngryMonkey.Cloud.Geography
```

#### .Net CLI<a name=".Net CLI"></a>
``cli
dotnet add package AngryMonkey.Cloud.Geography 
```
### Implementation<a name="Implementation"></a>

------------


#### NameSpace<a name="NameSpace"></a>

```cs     
using AngryMonkey.Cloud;
using AngryMonkey.Cloud.Geography;
```

#### Initialization<a name="Initialization"></a>
```cs
CloudGeographyClient cloudGeography = new CloudGeographyClient();
```
### What Can You Do With It<a name="What Can You Do With It"></a>

------------

##### Get all available countries<a name="Get all available countries"></a>
```cs
List<Country> countries = await cloudGeography.Countries.GetAllAsync();
```
##### Get multiple countries by their 2 or 3 letters code<a name="Get multiple countries by their 2 or 3 letters code"></a>
```cs
List<Country> countries = await cloudGeography.Countries.GetAsync("USA", "CA");
```
##### Get a specific country by its 2 or 3 letters code<a name="Get a specific country by its 2 or 3 letters code"></a>
```cs
Country country = await cloudGeography.Countries.GetAsync("US");
```
##### Get languages by a specific country<a name="Get languages by a specific country"></a>
```cs
List<CountryLanguage> languages = await cloudGeography.Languages.GetByCountryAsync("USA");
```
##### Get currencies by a specific country<a name="Get currencies by a specific country"></a>
```cs
List<CountryCurrency> currencies = await cloudGeography.Currencies.GetByCountryAsync("USA");
```
