---
title: Yrityksen käsite Common Data Servicessa
description: Tässä aiheessa kuvataan yritystietojen integraatiota Finance and Operationsin ja Common Data Servicen välillä.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 444bfc1698a206ca34e67f742df63431a3b02649
ms.sourcegitcommit: 7da8811f1a7db858efb76edb0bdf857a47d07600
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/27/2020
ms.locfileid: "3728410"
---
# <a name="company-concept-in-common-data-service"></a>Yrityksen käsite Common Data Servicessa

[!include [banner](../../includes/banner.md)]


Finance and Operationsissa käsite *Yritys* on sekä oikeudellinen että liiketoiminnallinen yksikkö. Se on myös tietojen suojauksen ja näkyvyyden raja. Käyttäjät työskentelevät aina yksittäisen yrityksen kontekstissa, ja suurin osa tiedoista on yrityksen omistamia.

Common Data Servicessa ei ole vastaavaa käsitettä. Lähin käsite on *liiketoimintayksikkö*, joka on ensisijaisesti tietoturvan ja näkyvyyden raja käyttäjätiedoille. Tällä käsitteellä ei ole sama oikeudellisia tai liiketoiminnan vaikutuksia kuin yrityksen käsitteellä.

Koska liiketoimintayksikkö ja yritys eivät ole vastaavia käsitteitä, ei ole mahdollista pakottaa yksi-yhteen (1:1)-vastaavuutta niiden välillä Common Data Service -integrointia varten. Koska käyttäjien on kuitenkin oletusarvoisesti pystyttävä näkemään samat tietueet sovelluksessa ja Common Data Servicessa, Microsoft on ottanut käyttöön uuden entiteetin Common Data Servicessa, jonka nimi on cdm\_Company. Tämä entiteetti vastaa sovelluksen Yritys-yksikköä. Jos haluat varmistaa, että tietueiden näkyvyys vastaa toisiaan sovelluksen ja Common Data Servicen välillä heti käyttöönotettaessa, suosittelemme seuraavaa tietojen määritystä Common Data Servicessa:

+ Jokaiselle Finance and Operationsin Yritys-tietueelle, jolle on otettu käyttöön kaksoiskirjoitus, luodaan liittyvä cdm\_Company-tietue.
+ Kun cdm\_Company-tietue luodaan ja otetaan käyttöön kaksoiskirjoitukselle, luodaan oletusliiketoimintayksikkö, jolla on sama nimi. Vaikka kyseiselle liiketoimintayksikölle luodaan automaattisesti oletusryhmä, liiketoimintayksikköä ei käytetä.
+ Luodaan erillinen omistajaryhmä, jolla on sama nimi. Se liittyy myös liiketoimintayksikköön.
+ Oletusarvoisesti minkä tahansa sovelluksessa luodun ja Common Data Serviceen kaksoiskirjoitetun tietueen omistajaksi määritetään DW Owner -ryhmä, joka on linkitetty liitettyyn liiketoimintayksikköön.

Seuraavassa kuvassa on esimerkki tästä tietojen määrityksestä Common Data Servicessa.

![Tietojen määritys Common Data Servicessa](media/dual-write-company-1.png)

Tämän määrityksen vuoksi kaikki USMF-yritykseen liittyvät tietueet omistaa ryhmä, joka on linkitetty USMF-liiketoimintayksikköön Common Data Servicessa. Tämän vuoksi jokainen käyttäjä, jolla on liiketoimintayksikön käyttöoikeusrooli, joka on määritetty liiketoimintayksikkötason näkyvyydelle, voi nyt nähdä kyseiset tietueet. Seuraavassa esimerkissä kerrotaan, miten ryhmiä voidaan käyttää kyseisten tietueiden oikeisiin käyttöoikeuksiin.

+ Myyntipäällikkö-rooli määritetään USMF Sales -tiimin jäsenille.
+ Käyttäjät, joilla on Myyntipäällikkö-rooli, voivat käyttää mitä tahansa tilin tietueita, jotka ovat saman liiketoiminta yksikön jäseniä.
+ USMF Sales -tiimi on linkitetty aiemmin mainittuun USMF-liiketoimintayksikköön.
+ Tämän vuoksi USMF Sales -tiimin jäsenet näkevät minkä tahansa tilin, jonka omistaa USMF DW, joka olisi tullut USMF-yrityksen entiteetistä Finance and Operationsissa.

![Miten ryhmiä voidaan käyttää](media/dual-write-company-2.png)

Kuten edellä olevassa kuvassa näkyy, tämä 1:1-yhteys liiketoimintayksikön, yrityksen ja tiimin välillä on vain lähtökohta. Tässä esimerkissä uusi Europe-liiketoimintayksikkö luodaan manuaalisesti Common Data Servicessa sekä DEMF:n että ESMF:n ylätasona. Tämä uusi pääliiketoimintayksikkö ei liity kaksoiskirjoittamiseen. Sen avulla voidaan kuitenkin antaa "EUR Sales"-tiimin jäsenille pääsy tilitietoihin sekä DEMF:ssä että ESMF:ssä asettamalla tietojen näkyvyydeksi **Ylätaso/aliliiketoimintayksikkö** liittyvässä käyttöoikeusroolissa.

Viimeinen aihe, josta keskustellaan, on se, miten kaksoiskirjoitus määrittää, mihin omistajaryhmään sen tulisi liittää tietueita. Tätä toimintaa ohjaa cdm\_Company-tietueen **Oletusomistajaryhmä**-kenttä. Kun cdm\_Company-tietueelle on otettu käyttöön kaksoiskirjoitus, laajennus luo automaattisesti liittyvän liiketoimintayksikön ja omistajaryhmän (jos sitä ei vielä ole) ja määrittää **Oletusomistajaryhmä**-kentän. Järjestelmänvalvoja voi muuttaa kentän arvoksi eri arvon. Järjestelmänvalvoja ei kuitenkaan voi tyhjentää kenttää niin kauan kuin entiteetti on kaksoiskirjoitustilassa.

> [!div class="mx-imgBorder"]
![Oletusomistajaryhmä-kenttä](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Yrityksen tietojen omistajuus ja esilataus

Common Data Service -integrointi tuo yrityksen pariteetin käyttämällä yritystunnusta tietojen omistajuuden ilmaisemiseen. Kuten seuraavassa kuvassa näkyy, kaikkia yrityskohtaisia entiteettejä laajennetaan siten, että niillä on monta-yhteen (N:1)-suhde cdm\_Company-entiteetin kanssa.

> [!div class="mx-imgBorder"]
![N:1-suhde yrityskohtaisen entiteetin ja cdm_Company-yksikön välillä](media/dual-write-bootstrapping.png)

+ Kun yritys on lisätty ja tallennettu, arvo tietueissa muuttuu vain luku -arvoksi. Siksi käyttäjien tulee varmistaa, että he valitsevat oikean yrityksen.
+ Vain tietueet, joissa on yritystietoja, voivat olla kaksoiskirjoituskelpoisia sovelluksen ja Common Data Servicen välillä.
+ Olemassa olevien Common Data Service -tietojen osalta on pian saatavilla järjestelmänvalvojan johtama esilatauskokemus.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Yrityksen nimen täyttäminen automaattisesti asiakkaiden aktivointisovelluksissa

Yrityksen nimi voidaan täyttää automaattisesti usealla eri tavalla asiakkaiden aktivointisovelluksissa.

+ Järjestelmänvalvoja voi määrittää oletusyrityksen valitsemalla **Lisäasetukset > Järjestelmä > Suojaus > Käyttäjät**. Avaa **Käyttäjä**-lomake ja määritä sitten **Organisaation tiedot** -osassa **Yrityksen oletusarvo lomakkeissa** -arvo.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Oletusyrityksen määrittäminen Organisaation tiedot -osassa":::

+ Jos sinulla on **Järjestelmäkäyttäjä**-entiteetin **Kirjoitus**-käyttöoikeus **Liiketoimintayksikkö**-tasolla, voit muuttaa oletusyrityksen missä tahansa lomakkeessa valitsemalla yrityksen avattavasta **Yritys**-luettelosta.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Yrityksen nimen muuttaminen uudessa tilissä":::

+ Jos sinulla on useamman kuin yhden yrityksen **Kirjoitus**-käyttöoikeus, voit vaihtaa oletusyrityksen valitsemalla toiselle yritykselle kuuluvan tietueen.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Tietueen valitseminen vaihtaa oletusyrityksen":::

+ Jos olet järjestelmän määrittäjä tai järjestelmänvalvoja ja haluat täyttää yrityksen tiedot automaattisesti mukautetussa lomakkeessa, voit käyttää [lomaketapahtumia](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Lisää JavaScript-viittaus kohteeseen **msdyn_/DefaultCompany.js** ja käytä seuraavia tapahtumia. Voit käyttää mitä tahansa valmista lomaketta, kuten **Tili**-lomaketta.

    + Lomakkeen **OnLoad**-tapahtuma: määritä **defaultCompany**-kenttä.
    + **Yritys**-kentän **OnChange**-tapahtuma: määritä **updateDefaultCompany**-kenttä.

## <a name="apply-filtering-based-on-the-company-context"></a>Suodatuksen käyttäminen yrityskontekstin perusteella

Voit käyttää mukautettujen lomakkeiden yrityskontekstiin tai vakiolomakkeisiin lisättyihin mukautettuihin valintakenttiin perustuvaa suodatusta avaamalla lomakkeen ja ottamalla yrityssuodatuksen käyttöön **Liittyvien tietueiden suodatus** -osassa. Tämä asetus on määritettävä jokaiselle valintakentälle, joka suodatetaan tietyn tietueen taustalla olevan yrityksen perusteella. Seuraavassa kuvassa on tämä asetus **Tili**-lomakkeessa.

:::image type="content" source="media/apply-company-context.png" alt-text="Yrityskontekstin käyttäminen":::

