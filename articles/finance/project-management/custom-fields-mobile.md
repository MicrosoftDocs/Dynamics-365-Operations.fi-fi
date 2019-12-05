---
title: Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssa ja Androidissa
description: Tässä ohjeaiheessa on yleisiä tapoja käyttää laajennuksia mukautettujen kenttien käyttöönottoon.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: c0c578ca44919671b67daeea51a9ec7687f755c9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773642"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Ota Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen mukautetut kentät käyttöön iOS:ssa ja Androidissa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on yleisiä tapoja käyttää laajennuksia mukautettujen kenttien käyttöönottoon. Ohje käsittelee seuraavia aiheita:

- Eri tietotyypit, joita mukautettu kenttäkehys tukee
- Miten näytetään luku- tai muokattavat kentät työaikaraportin merkinnöissä ja tallennetaan käyttäjän antamat arvot takaisin tietokantaan
- Vain luku -kenttien näyttäminen työaikaraportin otsikossa
- Muun mukautetun liiketoimintalogiikan integroiminen oletusarvojen syöttämiseen kenttiin ja lisätarkistuksen tekemiseksi

## <a name="audience"></a>Yleisö

Tämä ohjeaihe on tarkoitettu kehittäjille, jotka ovat integroimassa mukautettuja kenttiä Microsoft Dynamics 365 Project Timesheet -mobiilisovelluksen piiriin, joka on saatavilla Apple iOS:lle ja Google Androidille. Oletuksena on, että lukijat tuntevat X++-kehitystyön ja projektin työaikaraportin toiminnot.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Tietosopimus – TSTimesheetCustomField X++-luokka

**TSTimesheetCustomField** -luokka on X++-tietosopimusluokka, joka vastaa työaikaraportin toiminnon mukautettua kenttää koskevia tietoja. Mukautettujen kenttäobjektien luettelot välitetään sekä TSTimesheetDetails-tietosopimuksessa että TSTimesheetEntry-tietosopimuksessa, jolloin mobiilisovelluksen mukautetut kentät näkyvät.

- **TSTimesheetDetails** - Työaikaraportin otsikkosopimus.
- **TSTimesheetEntry** - Työaikaraportin tapahtumasopimus. Näiden objektien ryhmät, joilla on samat projektitiedot ja **timesheetLineRecId**-arvo, muodostavat rivin.

### <a name="fieldbasetype-types"></a>fieldBaseType (Tyypit)

**FieldBaseType**-objektin **TsTimesheetCustom**-ominaisuus määrittää sovelluksessa näkyvän kentän tyypin. Seuraavia **tyyppi**arvoja tuetaan.

| Tyypin arvo | Laji              | Muistiinpanot |
|-------------|-------------------|-------|
| 0           | Merkkijono (ja Enum) | Kenttä näkyy tekstikenttänä. |
| 1           | Kokonaisluku           | Arvo näkyy lukuna ilman desimaalipaikkoja. |
| 2           | Reaaliluku              | Arvo näkyy lukuna, jolla on desimaalipaikkoja.<p>Jos haluat, että todellinen arvo näkyy sovelluksessa valuuttana, käytä **fieldExtenededType**-ominaisuutta. **numberOfDecimals**-ominaisuuden avulla voit määrittää näytettävien desimaalien määrän.</p> |
| 3           | Päivämäärä              | Päivämäärämuodot määräytyvät käyttäjän **päivämäärä, kellonajan ja numeromuodon** asetuksella , joka on määritetty kohdassa **Kieli- ja maa-/alue** -asetukset kohdassa **Käyttäjäasetukset**. |
| 4           | Boolen arvo           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Jos **TSTimesheetCustomField**-objektissa ei ole **stringOptions**-ominaisuutta, käyttäjälle annetaan vapaamuotoinen tekstikenttä.

    **Stringlength**-ominaisuudella voidaan määrittää suurin sallittu merkkijonon pituus, jonka käyttäjät voivat kirjoittaa.

- Jos **TSTimesheetCustomField**-objektissa on **stringOptions**-ominaisuus, nämä luetteloelementit ovat ainoat arvot, joita käyttäjät voivat valita valintapainikkeiden avulla.

    Tässä tapauksessa merkkijonokenttä voi toimia Enum-arvona käyttäjämerkintää varten. Jos haluat tallentaa arvon tietokantaan luetteloluetteloksi, määritä merkkijonon arvo manuaalisesti takaisin Enum-arvoksi ennen tallennusta tietokantaan käyttämällä komentoketjua (Katso "Käytä komentoketjua TSTimesheetEntryService-luokassa, kun haluat tallentaa tuntilomake merkinnän sovelluksesta takaisin tietokantaan"-osassa, joka on jäljempänä tässä esimerkissä).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Tämän ominaisuuden avulla voit muotoilla todellisia arvoja valuutoiksi. Tämä menetelmä on käytettävissä vain, kun **fieldBaseType**-arvo on **reaaliluku**.

- **TSCustomFieldExtendedType:None** – Muotoilua ei käytetä.
- **TSCustomFieldExtendedType::Valuutta** – Muotoile arvo valuuttana.

    Kun valuuttamuotoilu on käytössä, voit käyttää **stringValue**-kenttää ja siirtääksesi valuuttakoodin, joka näytetään sovelluksessa. Arvo on vain luku -arvo.

    **realValue**-kenttä sisältää rahamäärän, joka on tallennettava tietokantaan.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Tämän ominaisuuden avulla voit määrittää, missä sovelluksessa mukautetun kentän pitäisi näkyä.

- **TSCustomFieldSection::Otsikko** – Kenttä näkyy sovelluksen **Katso lisätietoja** -osassa. Nämä kentät ovat aina vain luku -muotoisia.
- **TSCustomFieldSection::Tivi** – Kenttä tulee näkyviin, kun kaikki valmiiksi määritetyt rivikentät ovat aikaraporttikentissä. Nämä kentät voivat olla joko muokattavia tai vain luku -muotoisia.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Tämä ominaisuus määrittää kentän, kun sovelluksen luomat arvot tallennetaan takaisin tietokantaan.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Tämä ominaisuus määrittää kentän, kun sovelluksen luomat arvot tallennetaan takaisin tietokantaan.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että käyttäjät voivat muokata tuntilomakkeen merkintäosan kenttää. Määritä ominaisuuden arvoksi **Ei**, jos haluat tehdä kentästä vain luku -muotoisen.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Määrittämällä tämän ominaisuuden arvoksi **Kyllä** voit määrittää, että tuntilomakkeen merkintäosan kentän tulisi olla pakollinen.

### <a name="label-str"></a>label (str)

Tämä ominaisuus määrittää otsikon, joka näkyy sovelluksen kentän vieressä.

### <a name="stringoptions-list-of-strings"></a>stringOptions (merkkijonojen luettelo)

Tämä ominaisuus on käytettävissä vain, kun **fieldbasetype** -arvo on **Merkkijono**. Jos **stringOptions** on määritetty, valintapainikkeiden kautta valittavissa olevat merkkijonoarvot (Radiopainikkeet) määritetään luettelon merkkijonojen avulla. Jos merkkijonoja ei anneta, merkkijonokentän vapaatekstin syöttö on sallittu (esimerkin löydät kohdassa "komentoketjun käyttäminen Tstimessheedistryservice-luokassa, jolloin tuntilomakekohta tallennetaan sovelluksesta tietokantaan uudelleen" -osassa myöhemmin tässä aiheessa).

### <a name="stringlength-int"></a>stringLength (int)

Tämä ominaisuus määrittää merkkijonokentän enimmäispituuden. Se on käytettävissä vain, kun **fieldBaseType**-arvo on **Merkkijono**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Tämä ominaisuus määrittää todellisen kentän desimaalipaikkojen määrän. Se on käytettävissä vain, kun **fieldBaseType**-arvo on **Reaaliarvo**.

### <a name="ordersequence-int"></a>orderSequence (int)

Tämä ominaisuus määrittää, missä järjestyksessä mukautetut kentät näkyvät sovelluksessa, kun määritettynä on useita mukautettuja kenttiä. Alanumeroita käyttävät kentät näytetään ensin.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

**Boolean**-tyypin kentissä tämä ominaisuus siirtää kentän totuusarvon palvelimen ja sovelluksen välille.

### <a name="guidvalue-guid"></a>guidValue (guid)

**GUID**-tyypin kentissä tämä ominaisuus siirtää kentän yksilöivän tunnisteen palvelimen ja sovelluksen välille.

### <a name="int64value-int64"></a>int64Value (Int64)

**Int64**-tyypin kentissä tämä ominaisuus siirtää kentän Int64-arvon palvelimen ja sovelluksen välille.

### <a name="intvalue-int"></a>intValue (int)

**Int**-tyypin kentissä tämä ominaisuus siirtää kentän Int-arvon palvelimen ja sovelluksen välille.

### <a name="realvalue-real"></a>realValue (real)

**Reaaliarvo**-tyypin kentissä tämä ominaisuus siirtää kentän reaaliarvon palvelimen ja sovelluksen välille .

### <a name="stringvalue-str"></a>stringValue (str)

**Merkkijono**-tyypin kentissä tämä ominaisuus siirtää kentän merkkijonoarvon palvelimen ja sovelluksen välille. Sitä käytetään myös sellaisissa kentissä, joiden **reaaliarvo** on muotoiltu valuutaksi. Näiden kenttien osalta ominaisuutta käytetään valuuttakoodin välittämiseen sovellukseen.

### <a name="datevalue-date"></a>dateValue (date)

**Päivämäärä**-tyypin kentissä tämä ominaisuus siirtää kentän päivämäärän palvelimen ja sovelluksen välille.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mukautetun kentän näyttäminen ja tallentaminen tuntilomakemerkinnän osassa

Alla on näyttökuva aikaraportin merkinnän luomisesta mobiilisovelluksesta. Se näyttää valmiiksi määritetyt kentät ja mukautetun kentän aikamerkintäosassa nimeltä "Testimerkkijono" ja enum-arvo "Toinen vaihtoehto" on jo asetettu.

![Testimerkkijonon mukautettu kenttä sovelluksessa](media/timesheet-entry.jpg)



Alla on kuvakaappaus käyttäjän mobiilisovelluksesta, jossa valitaan jokin käytettävissä olevista enum-asetuksista Testimerkkijono-kohtaan.  Kaksi vaihtoehtoa ovat "ensimmäinen vaihtoehto" ja "toinen vaihtoehto", jotka näkyvät valintapainikkeina. Toinen vaihtoehto on valittuna.

![Testimerkkijonon mukautetun kentän valintapainikkeita (valintanappeja)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Laajenna TSTimesheetLine-taulukkoa niin, että siinä on mukautettu kenttä

Tyypillisissä skenaarioissa on todennäköistä, että tuntilomakemerkinnän mukautetun kentän tiedot tallennetaan TSTimesheetLine-tauluun. Muita tauluja voidaan kuitenkin käyttää, jos tiedot voidaan noutaa annetun TSTimesheetTrans-tietueen perusteella tai jos niillä ei ole tiettyä tietuetaustaa (Jos esimerkiksi kenttä on määritetty vain luku -tilaan projektin parametreissä).

Huomaa, että mukautettujen kenttien ei tarvitse sisältää tietokantatietuetta. Ne voidaan luoda dynaamisesti X++-logiikan perusteella. Tämä lähestymistapa voi olla hyödyllinen vain luku -tilassa olevissa skenaarioissa (lisätietoja on kohdassa "komentoketjun käyttäminen TSTimesheetDetails-luokassa, buildCustomFieldListForHeader-menetelmä, joka täyttää tuntilomakkeen tiedot" -osassa, jossa on esimerkki dynaamisesti tuotetuista mukautetuista kenttäarvoista.)

Alla on kuvakaappaus Visual Studion sovellusobjektipuusta. Siinä näkyy TSTimesheetLine-taulun laajennus ja TestLineString-kenttä on lisätty mukautetuksi kentäksi.

![Merkkijono](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän tuntilomakemerkinnän osassa.

Tämä koodi ohjaa sovelluksen kentän näyttöasetuksia. Se määrittää esimerkiksi kentän tyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.

Seuraavassa esimerkissä näkyy aikamerkintöjen merkkijonokenttä. Tässä kentässä on kaksi vaihtoehtoa **Ensimmäinen vaihtoehto** ja **Toinen vaihtoehto**, jotka ovat käytettävissä valintapainikkeiden kautta (valintanapit). Sovelluksen kenttä liitetään **TestLineString**-kenttään, joka lisätään TSTimesheetLine-tauluun.

Huomaa **TSTimesheetCustomField::newFromMetatdata()**-menetelmän käyttäminen mukautettujen kenttien ominaisuuksien alustamisen yksinkertaistamiseksi: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** ja **numberOfDecimals**. Voit myös määrittää nämä parametrit manuaalisesti kuten haluat.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Käytä komentoketjua TSTimesheetEntry-luokan buildCustomFieldListForEntry-menetelmässä, kun haluat syöttää arvoja tuntilomakkeeseen

**buildCustomFieldListForEntry**-menetelmällä syötetään arvoja mobiilisovellukseen tallennettujen työaikaraporttien riveille. Se ottaa TSTimesheetTrans-tietueen parametriksi. Tietueen kenttiä voidaan käyttää sovelluksen mukautetun kentän arvon täyttämiseen.

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Käyttämällä TSTimesheetEntryService-luokan komentoketjua voit tallentaa tuntilomakemerkinnän sovelluksesta takaisin tietokantaan.

Jos haluat tallentaa mukautetun kentän takaisin tietokantaan tyypillisessä käytössä, sinun on laajennettava useita menetelmiä:

- **timesheetLineNeedsUpdating**-menetelmän avulla määritetään, onko käyttäjä muuttanut rivitietuetta sovelluksessa ja pitääkö se tallentaa tietokantaan. Jos suorituskyky ei ole ongelma, tätä menetelmää voidaan yksinkertaistaa niin, että se palauttaa aina arvon **Tosi**.
- **populateTimesheetLineFromEntryDuringCreate**- ja **populateTimesheetLineFromEntryDuringUpdate** -menetelmiä voidaan jatkaa siten, että ne syöttävät arvot TSTimesheetLine-tietokantatietueeseen TSTimesheetEntry-tietueesta annetusta tietosopimustietueesta. Seuraavassa esimerkissä ilmoitetaan, miten tietokantakentän ja syöttökentän välinen vastaavuus tehdään manuaalisesti X++-koodin avulla.
- **populateTimesheetWeekFromEntry**-menetelmää voidaan myös jatkaa, jos **TSTimesheetEntry**-objektiin yhdistettävän mukautetun kentän on kirjoitettava takaisin TSTimesheetLineweek-tietokantatauluun.

> [!NOTE]
> Seuraavassa esimerkissä tallennetaan **firstOption**- tai **secondOption**-arvo, jonka käyttäjä valitsee tietokantaan raakamerkkijonoarvona. Jos tietokantakenttä on **Enum**-tyypin kenttä, arvot voidaan määrittää manuaalisesti Enum-arvoksi ja tallentaa sitten tietokantataulun Enum-kenttään.

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mukautetun kentän näyttäminen tuntilomakkeen otsikossa

Alla on näyttökuva aikaraportin käyttäjän mobiilisovelluksesta, jossa näkyy käyttäjän tuntilomakenäkymä. Lisätietoja-painike on valittu oikeasta yläkulmasta, jolloin näkyviin tulee Näytä lisätiedot -vaihtoehto.  

![Näytä lisätietoja -komento](media/show-more.png)

Alla on näyttökuva aikaraportin käyttäjän mobiilisovelluksesta, jossa näkyy tuntilomakkeen Lisää-osa. Tuntilomakkeen otsikko-osaan on lisätty mukautettu kenttä, jonka nimi on Tämän tuntilomakkeen käyttöaste (laskettu mukautettu kenttä). Vain luku -arvo 0,667 on määritetty mukautettuun kenttään.

![Lisää-osa](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Laajenna TSTimesheetTable-taulukkoa niin, että siinä on mukautettu kenttä

Tyypillisissä skenaarioissa on todennäköistä, että otsikon mukautetun kentän tiedot haetaan TSTimesheetLine-taulusta. Muita tauluja voidaan kuitenkin käyttää, jos tiedot voidaan noutaa annetun TSTimesheetTable-tietueen perusteella tai jos niillä ei ole tiettyä tietuetaustaa (Jos esimerkiksi kenttä on määritetty vain luku -tilaan projektin parametreissä).

Huomaa, että mukautettujen kenttien ei tarvitse sisältää tietokantatietuetta. Ne voidaan luoda dynaamisesti X++-logiikan perusteella. Seuraava esimerkki osoittaa tämän lähestymistavan.

Otsikko-osan kentät ovat aina vain luku -tilassa sovelluksessa.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Käytä komentoketjua TSTimesheetSettings-luokan buildCustomFieldList-menetelmässä, kun haluat näyttää kentän otsikon osassa.

Tämä koodi ohjaa sovelluksen kentän näyttöasetuksia. Se määrittää esimerkiksi kentän tyypin, otsikon, sen, onko kenttä pakollinen, ja missä osassa kenttä näkyy.

Seuraavassa esimerkissä näkyy laskettu arvo sovelluksen otsikko-osassa.

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Käytä komentoketjua TSTimesheetDetails-luokan buildCustomFieldListForHeader-menetelmässä, kun haluat täyttää arvoja tuntilomakkeen tietoihin

**buildCustomFieldListForHeader**-menetelmällä täytetään arvoja mobiilisovellukseen työaikaraporttien otsikkotietoihin. Se ottaa TSTimesheetTable-tietueen parametriksi. Tietueen kenttiä voidaan käyttää sovelluksen mukautetun kentän arvon täyttämiseen. Seuraava esimerkki ei lue mitään tietokannan arvoja. Sen sijaan se luo X++-logiikan avulla lasketun arvon, joka näkyy sovelluksessa.


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Muut konfiguroitavuus- ja laajennettavuusmahdollisuudet

### <a name="adding-additional-validation-for-the-app"></a>Lisävahvistuksen lisääminen sovellukselle

Työaikaraporttien toiminnallisuuden nykyinen logiikka tietokannan tasolla toimii edelleen odotetulla tavalla. Jos haluat keskeyttää Tallenna- tai Lähetä-toimintojen päättymisen ja näyttää tietyn virhesanoman, voit lisätä koodiin **heittovirheen ("sanoma käyttäjälle")** komentolaajennusketjun kautta. Seuraavassa on kolme esimerkkiä hyödyllisistä laajennettavien menetelmien menetelmistä:

- Jos **validateWrite** TSTimesheetLine-taulussa palauttaa arvon **Epätosi** aikaraportin rivin tallennustoiminnon aikana, mobiilisovelluksessa näkyy virhesanoma.
- Jos **validateSubmit** TSTimesheetTable-taulussa palauttaa arvon **Epätosi** aikaraportin sovelluksen esittämisen aikana, käyttäjälle näytetään virhesanoma.
- Logiikka, joka täyttää kentät (esimerkiksi **Rivin ominaisuus**) TSTimesheetLine-taulun **insert**-menetelmän aikana, suoritetaan edelleen.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Käyttövalmiiden kenttien piilottaminen ja merkitseminen vain luku -muodossa konfiguroinnin kautta

Projektin parametreistä voit määrittää, että käyttövalmiit kentät ovat vain luku -muotoisia tai piilotettuja mobiilisovelluksessa. Määritä valinnat **Mobiililaitteen aikaraportti** -osalle **Aikaraportti**-välilehdellä **Projektinhallinta- ja kirjanpidon parametrit** - sivulla.

![Projektiparametrit](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Valintaan käytettävissä olevien tehtävien muuttaminen laajennusten kautta

Projektin valintaan käytettävissä olevat toiminnot täytetään **getActivitiesForProject()**- ja **getActivityQuery()**-menetelmien avulla **TsTimesheetProjectService**-luokassa. Voit käyttää komentoketjua, kun haluat muuttaa tätä toimintatapaa niin, että se vastaa tiettyä projektia varten valittavissa olevien toimintojen liiketoimintaskenaariota.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Oletusprojektiluokan syöttäminen työaikaraportin merkinnöille

Oletusprojektiluokan määritys työaikaraportin merkinnöissä tapahtuu kolmella tasolla. Voit käyttää komentoketjua, kun haluat laajentaa käyttäytymistä millä tahansa tai kaikilla näillä tasoilla halutun toiminnan saavuttamiseksi. Seuraavaa hierarkiaa käytetään:

1. Sovellus yrittää sijoittaa oletusluokan projektiresurssista. Tämä oletus luokka on määritetty **getCurrentUserResource**- ja **getDelegatedResourcesForCurrentUser**-menetelmille **TSTimesheetSettingsService**-luokassa.
2. Jos oletusluokkaa ei ole projektiresurssitasolla, sovellus yrittää vetää sen projektitehtävästä. Tämä oletusluokka määritetään **getActivitiesForProject**-menetelmällä **TSTimesheetProjectService**-luokassa.
3. Jos oletusluokkaa ei ole projektitehtävätasolla, oletuskategoria otetaan projektin parametreista. Tämä oletusluokka määritetään **getProjectDetailsbyRule**-menetelmällä **TSTimesheetProjectService**-luokassa.
