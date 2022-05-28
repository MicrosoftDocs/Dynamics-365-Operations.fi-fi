---
title: Tuotannon käyttöliittymän mukauttaminen
description: Tässä aiheessa käsitellään nykyisten lomakkeiden laajentamista tai uusien lomakkeiden ja painikkeiden luontia tuotannon käyttöliittymää varten.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ad5037442f27a5068b38613655591f1298808eac
ms.sourcegitcommit: 28537b32dbcdefb1359a90adc6781b73a2fd195e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712940"
---
# <a name="customize-the-production-floor-execution-interface"></a>Tuotannon käyttöliittymän mukauttaminen

[!include [banner](../includes/banner.md)]

Kehittäjät voivat laajentaa nykyisiä lomakkeita tai luoda omia lomakkeita ja painikkeita tuotannon käyttöliittymää varten. Kun näiden uusien elementtien koodi on lisätty, järjestelmänvalvojat tai työnjohtajat voivat lisätä ne helposti liittymään määrityksen vakio-ohjausobjekteilla.

Seuraavassa on esimerkkejä mahdollisista ratkaisuista, jos päälomakkeessa tarvitaan uusia sarakkeita:

- Laajenna `JmgProductionFloorExecutionMainGrid`-lomake ja lisää kentät.
- Luo uusi lomake ja lisää se uutena päänäkymänä (välilehtenä).

## <a name="add-a-new-button-action"></a>Uuden painikkeen (toiminnon) lisääminen

Uusi painike (toiminto) lisätään luomalla mukautetun toiminnon toteuttava luokka seuraavasti:

1. Luo uusi `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`-niminen luokka, jossa

    - `<ExtensionPrefix>` määrittää ratkaisun yksilöivästi käyttämällä yleensä yrityksen nimeä
    - `<ActionName>` on luokan yksilöivä nimi. Se ilmaisee yleensä toiminnon tyypin.

1. Uuden luokan on laajennettava `JmgProductionFloorExecutionAction`-luokkaa.
1. Ohita kaikki tarvittavat menetelmät.

Esimerkeissä tarkastellaan seuraavien luokkien koodia:

- `JmgProductionFloorExecutionBreakAction` – sellaisen yksinkertaisen toiminnon luokka, jossa ei tarvita tietueita.
- `JmgProductionFloorExecutionReportFeedbackAction` – tässä luokassa on monimutkaisia toimintoja.

Kun olet valmis, uusi painike (toiminto) on lisätään automaattisesti luetteloon **Suunnittele välilehtiä** -sivulla Microsoft Dynamics 365 Supply Chain Managementissa. Tällä sivulla käyttäjän (tai järjestelmänvalvojan tai työnjohtajan) on helppo lisätä se ensi- tai toissijaiselle työkaluriville vakiopainikkeiden tavoin. Lisätietoja on kohdassa [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Uuden päänäkymän lisääminen

1. Luo uusi lomake, jossa on toivotut elementit ja toiminnot. Huomaa, että tämä lomake on uusi lomake eikä laajennus. Anna lomakkeen nimeksi `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, jossa

    - `<ExtensionPrefix>` määrittää ratkaisun yksilöivästi käyttämällä yleensä yrityksen nimeä
    - `<FormName>` on lomakkeen yksilöivä nimi.

1. Luo `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`-niminen valikkovaihtoehto.
1. Luo `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`-niminen laajennus, jossa `getMainMenuItemsList`-menetelmää laajennetaan lisäämällä uusi valikkokohde luetteloon. Seuraavassa koodissa on esimerkki.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Kun olet valmis, uusi näkymä lisätään automaattisesti **Päänäkymä**-yhdistelmäruudun luetteloon Supply Chain Managementin **Suunnittele välilehtiä** -sivulla. Tällä sivulla käyttäjän (tai järjestelmänvalvojan tai työnjohtajan) on helppo lisätä se uusiin tai aiemmin luotuihin välilehtiin vakiopäänäkymien tavoin. Lisätietoja on kohdassa [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Tietonäkymän lisääminen

1. Luo uusi lomake, jossa on toivotut elementit ja toiminnot. Huomaa, että tämä lomake on uusi lomake eikä laajennus. Anna lomakkeen nimeksi `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, jossa 

    - `<ExtensionPrefix>` määrittää ratkaisun yksilöivästi käyttämällä yleensä yrityksen nimeä
    - `<FormName>` on lomakkeen yksilöivä nimi.

1. Luo `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`-niminen valikkovaihtoehto.
1. Luo `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`-niminen laajennus, jossa `getDetailsMenuItemList`-menetelmää laajennetaan lisäämällä uusi valikkokohde luetteloon.

Kun olet valmis, uudet tiedot lisätään automaattisesti **Tietonäkymä**-yhdistelmäruudun luetteloon Supply Chain Managementin **Suunnittele välilehtiä** -sivulla. Tällä sivulla käyttäjän (tai järjestelmänvalvojan tai työnjohtajan) on helppo lisätä se uusiin tai aiemmin luotuihin välilehtiin vakiotietonäkymien tavoin. Lisätietoja on kohdassa [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Numeronäppäimistön lisääminen lomakkeeseen tai ikkunaan

Seuraavassa esimerkki osoittaa, miten numeronäppäimistöt lisätään lomakkeeseen.

1. Kunkin lomakkeen sisältävien numeronäppäimistön ohjausobjektien määrän on oltava yhtä suuri kuin kyseisen lomakkeen numeronäppäimistöjen määrä.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Määritä kunkin numeronäppäimistön ohjausobjektin toiminta ja yhdistä kukin numeronäppäimistön ohjausobjekti lomakkeen numeronäppäimistöosaan.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Numeronäppäimistön käyttäminen ponnahdusikkunana

Seuraava esimerkki näyttää yhden tavan, jolla ponnahdusikkunan numeronäppäimistön ohjausobjekti määritetään.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Seuraava esimerkki näyttää yhden tavan kutsua ponnahdusikkunan numeronäppäimistöä.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Päivämäärä- ja aikaohjausobjektejen lisääminen lomakkeeseen tai valintaikkunaan

Tässä osassa kerrotaan, miten lomakkeeseen tai valintaikkunaan lisätään päivämäärä- ja aikaohjausobjekteja. Kosketuskäyttöisten päivämäärä- ja aikaohjausten avulla työntekijät voivat määrittää päivämääriä ja aikoja. Seuraavien näyttökuvien avulla voit nähdä, miten ohjausobjektit yleensä näkyvät sivulla. Aikaohjausobjekti sisältää sekä 12- että 24 tunnin versiot. Näyttöön tulee sen käyttäjätilin asetusjoukko, jota liittymä käyttää.

![Esimerkki päivämääräohjausobjektista.](media/pfe-customize-date-control.png "Esimerkki päivämääräohjausobjektista")

![Esimerkki aikaohjausobjekstista, jossa on 12 tunnin kello.](media/pfe-customize-time-control-12h.png "Esimerkki aikaohjausobjekstista, jossa on 12 tunnin kello")

![Esimerkki aikaohjausobjekstista, jossa on 24 tunnin kello.](media/pfe-customize-time-control-24h.png "Esimerkki aikaohjausobjekstista, jossa on 24 tunnin kello")

Seuraavassa esitetään esimerkki siitä, miten lomakkeeseen lisätään päivämäärä- ja aikaohjausobjekteja.

1. Lisää lomakkeeseen ohjausobjekti jokaista lomakkeen päivämäärän ja ajan hallintaa varten. (Ohjausobjektien määrän on oltava yhtä suuri kuin lomakkeen päivämäärä- ja aikaohjausobjektienkin.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Ilmoita pakolliset muuttujat (tyyppi `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Luo menetelmät, joilla päivämäärä/aika-ohjausobjektit päivittävät päivämäärän/ajan. Seuraavassa esimerkissä on yksi tällainen menetelmä.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Määritä kunkin päivämäärä/aika-ohjausobjektin toiminta ja yhdistä kukin ohjausobjekti lomakkeen osaan. Seuraavassa esimerkissä kerrotaan, miten tiedot määritetään alkamispäivämäärä- ja alkamisaika-ohjausobjekteille. Voit lisätä vastaavan koodin loppupäivämäärä- ja loppuaika-ohjausobjekteille (ei näytetä).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Jos tarvitset vain päivämäärän ohjausobjektin, voit ohittaa ajan ohjausobjektin asetuksen ja vain määrittää päivämäärän ohjausobjektin seuraavan esimerkin mukaisesti:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Lisäresurssit

- [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-styles.md)
- [Tuotannon käyttöliittymän suunnitteleminen](production-floor-execution-tabs.md)
