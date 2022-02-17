---
title: Yrityksen käsite Dataversessa
description: Tässä aiheessa kuvataan yrityksen tietojen intergraatiota Finance and Operationsin ja Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3657e41363ca6c1ce8eabfeaf3ba6da9b93f5e2a
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061023"
---
# <a name="company-concept-in-dataverse"></a>Yrityksen käsite Dataversessa

[!include [banner](../../includes/banner.md)]




Finance and Operationsin *yritys*-käsite on sekä oikeudellinen että liiketoiminnallinen yksikkö. Se on myös tietojen suojauksen ja näkyvyyden raja. Käyttäjät työskentelevät aina yksittäisen yrityksen kontekstissa, ja suurin osa tiedoista on yrityksen omistamia.

Dataversessa ei ole vastaavaa käsitettä. Lähin käsite on *liiketoimintayksikkö*, joka on ensisijaisesti tietoturvan ja näkyvyyden raja käyttäjätiedoille. Tällä käsitteellä ei ole sama oikeudellisia tai liiketoiminnan vaikutuksia kuin yrityksen käsitteellä.

Koska liiketoimintayksikkö ja yritys eivät ole vastaavia käsitteitä, ei ole mahdollista pakottaa yksi-yhteen (1:1)-vastaavuutta niiden välillä Dataverse -integrointia varten. Koska käyttäjien on kuitenkin oletusarvoisesti pystyttävä näkemään samat rivit sovelluksessa ja Dataversessa, Microsoft on ottanut käyttöön uuden taulun Dataversessa, jonka nimi on cdm\_Company. Tämä taulu vastaa sovelluksen Yritys-taulua. Jos haluat varmistaa, että rivien näkyvyys vastaa toisiaan sovelluksen ja Dataversen välillä heti käyttöönotettaessa, suosittelemme seuraavaa tietojen määritystä Dataversessa:

+ Jokaiselle taloushallinnon ja toimintojen Yritys-riville, jolle on otettu käyttöön kaksoiskirjoitus, luodaan liittyvä cdm\_Company-rivi.
+ Kun cdm\_Company-rivi luodaan ja otetaan käyttöön kaksoiskirjoitukselle, luodaan oletusliiketoimintayksikkö, jolla on sama nimi. Vaikka kyseiselle liiketoimintayksikölle luodaan automaattisesti oletusryhmä, liiketoimintayksikköä ei käytetä.
+ Luodaan erillinen omistajaryhmä, jolla on sama nimi. Se liittyy myös liiketoimintayksikköön.
+ Oletusarvoisesti minkä tahansa sovelluksessa luodun ja Dataverseen kaksoiskirjoitetun rivin omistajaksi määritetään DW Owner -ryhmä, joka on linkitetty liitettyyn liiketoimintayksikköön.

Seuraavassa kuvassa on esimerkki tästä tietojen määrityksestä Dataversessa.

![Tietojen määritys Dataversessa.](media/dual-write-company-1.png)

Tämän määrityksen vuoksi kaikki USMF-yritykseen liittyvät rivit omistaa ryhmä, joka on linkitetty USMF-liiketoimintayksikköön Dataversessa. Tämän vuoksi jokainen käyttäjä, jolla on liiketoimintayksikön käyttöoikeusrooli, joka on määritetty liiketoimintayksikkötason näkyvyydelle, voi nyt nähdä kyseiset rivit. Seuraavassa esimerkissä kerrotaan, miten ryhmiä voidaan käyttää antamaan kyseisille riveille oikeat käyttöoikeudet.

+ Myyntipäällikkö-rooli määritetään USMF Sales -tiimin jäsenille.
+ Käyttäjät, joilla on Myyntipäällikkö-rooli, voivat käyttää mitä tahansa tilin rivejä, jotka ovat saman liiketoimintayksikön jäseniä.
+ USMF Sales -tiimi on linkitetty aiemmin mainittuun USMF-liiketoimintayksikköön.
+ Tämän vuoksi USMF Sales -tiimin jäsenet näkevät minkä tahansa tilin, jonka omistaa USMF DW, joka olisi tullut USMF-yrityksen taulusta taloushallinnossa ja toiminnoissa.

![Miten ryhmiä voidaan käyttää.](media/dual-write-company-2.png)

Kuten edellä olevassa kuvassa näkyy, tämä 1:1-yhteys liiketoimintayksikön, yrityksen ja tiimin välillä on vain lähtökohta. Tässä esimerkissä uusi Europe-liiketoimintayksikkö luodaan manuaalisesti Dataversessa sekä DEMF:n että ESMF:n ylätasona. Tämä uusi pääliiketoimintayksikkö ei liity kaksoiskirjoittamiseen. Sen avulla voidaan kuitenkin antaa "EUR Sales"-tiimin jäsenille pääsy tilitietoihin sekä DEMF:ssä että ESMF:ssä asettamalla tietojen näkyvyydeksi **Ylätaso/aliliiketoimintayksikkö** liittyvässä käyttöoikeusroolissa.

Viimeinen käsiteltävä aihe on, miten kaksoiskirjoitus määrittää, mihin omistajaryhmään sen tulisi liittää tilejä. Tätä toiminnallisuutta ohjaa **Oletusomistajaryhmä**-sarake kohdassa cdm\_Yrityksen rivi. Kun cdm\_Yrityksen rivillä on otettu käyttöön kaksoiskirjoitus, laajennus luo automaattisesti liittyvän liiketoimintayksikön ja omistajaryhmän (jos sitä ei vielä ole) ja määrittää **Oletusomistajaryhmä**-sarakkeen. Järjestelmänvalvoja voi muuttaa sarakkeen arvoksi eri arvon. Järjestelmänvalvoja ei kuitenkaan voi tyhjentää saraketta niin kauan kuin taulu on kaksoiskirjoitustilassa.

> [!div class="mx-imgBorder"]
![Oletusomistajaryhmä-sarake.](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Yrityksen tietojen omistajuus ja esilataus

Dataverse -integrointi tuo yrityksen pariteetin käyttämällä yritystunnusta tietojen omistajuuden ilmaisemiseen. Kuten seuraavassa kuvassa näkyy, kaikkia yrityskohtaisia tauluja laajennetaan siten, että niillä on monta-yhteen (N:1)-suhde cdm\_Yritys-taulun kanssa.

> [!div class="mx-imgBorder"]
![N:1-suhde yrityskohtaisen taulukon ja cdm_Company-taulukon välillä.](media/dual-write-bootstrapping.png)

+ Kun yritys on lisätty ja tallennettu, arvo riveillä muuttuu vain luku -arvoksi. Siksi käyttäjien tulee varmistaa, että he valitsevat oikean yrityksen.
+ Vain rivit, joilla on yritystietoja, voivat olla kaksoiskirjoituskelpoisia sovelluksen ja Dataversen välillä.
+ Olemassa olevien Dataverse -tietojen osalta on pian saatavilla järjestelmänvalvojan johtama esilatauskokemus.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Yrityksen nimen täyttäminen automaattisesti asiakkaiden aktivointisovelluksissa

Yrityksen nimi voidaan täyttää automaattisesti usealla eri tavalla asiakkaiden aktivointisovelluksissa.

+ Järjestelmänvalvoja voi määrittää oletusyrityksen valitsemalla **Lisäasetukset > Järjestelmä > Suojaus > Käyttäjät**. Avaa **Käyttäjä**-lomake ja määritä sitten **Organisaation tiedot** -osassa **Yrityksen oletusarvo lomakkeissa** -arvo.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Oletusyrityksen määrittäminen Organisaation tiedot -osassa":::

+ Jos sinulla on **Järjestelmäkäyttäjä**-taulun **Kirjoitus**-käyttöoikeus **Liiketoimintayksikkö**-tasolla, voit muuttaa oletusyrityksen missä tahansa lomakkeessa valitsemalla yrityksen avattavasta **Yritys**-luettelosta.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Yrityksen nimen muuttaminen uudessa tilissä":::

+ Jos sinulla on useamman kuin yhden yrityksen **Kirjoitus**-käyttöoikeus, voit vaihtaa oletusyrityksen valitsemalla toiselle yritykselle kuuluvan rivin.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Rivin valitseminen vaihtaa oletusyrityksen.":::

+ Jos olet järjestelmän määrittäjä tai järjestelmänvalvoja ja haluat täyttää yrityksen tiedot automaattisesti mukautetussa lomakkeessa, voit käyttää [lomaketapahtumia](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Lisää JavaScript-viittaus kohteeseen **msdyn_/DefaultCompany.js** ja käytä seuraavia tapahtumia. Voit käyttää mitä tahansa valmista lomaketta, kuten **Tili**-lomaketta.

    + Lomakkeen **OnLoad**-tapahtuma: määritä **defaultCompany**-sarake.
    + **Yritys**-sarakkeen **OnChange**-tapahtuma: määritä **updateDefaultCompany**-sarake.

## <a name="apply-filtering-based-on-the-company-context"></a>Suodatuksen käyttäminen yrityskontekstin perusteella

Voit käyttää mukautettujen lomakkeiden yrityskontekstiin tai vakiolomakkeisiin lisättyihin mukautettuihin valintasarakkeisiin perustuvaa suodatusta avaamalla lomakkeen ja ottamalla yrityssuodatuksen käyttöön **Liittyvien tietueiden suodatus** -osassa. Tämä asetus on määritettävä jokaiselle valintasarakkeelle, joka suodatetaan tietyn rivin taustalla olevan yrityksen perusteella. Seuraavassa kuvassa on tämä asetus **Tili**-lomakkeessa.

:::image type="content" source="media/apply-company-context.png" alt-text="Yrityskontekstin käyttäminen.":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]