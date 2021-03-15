---
title: Laitteen määrittäminen käyttämään tuotannon käyttöliittymää
description: Tuotannon käyttöliittymä määritetään jokaiselle tuotannon laitteelle. Yritykset yleensä määrittävät jokaisen laitteen eri tavalla sen perusteella, mikä on laitteen tarkoitus. Yrityksellä voi esimerkiksi olla yksi laite vastaanotossa, jossa työntekijät kuittaavat itsensä sisään ja ulos, ja toinen tuotantotiloissa, joissa työntekijät hallitsevat töitään.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d4529af21d9673512889b17aeb1e7fbd49969cdc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966273"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a>Laitteen määrittäminen käyttämään tuotannon käyttöliittymää

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tuotannon käyttöliittymä määritetään jokaiselle tuotannon laitteelle. Yritykset yleensä määrittävät jokaisen laitteen eri tavalla sen perusteella, mikä on laitteen tarkoitus. Yrityksellä voi esimerkiksi olla yksi laite vastaanotossa, jossa työntekijät kuittaavat itsensä sisään ja ulos, ja toinen tuotantotiloissa, joissa työntekijät hallitsevat töitään.

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a>Tietyn laitteen määritysten ja suodattimen määrittäminen

Laitteen määritykset ja työsuodattimet määritetään kirjautumalla **Tuotantoliittymä**-sivulle sillä tilillä, jonka käyttöoikeusrooli sisältää *Ajanseurannan työnjohto* -tehtävän. (Heti käytettävistä käyttöoikeusrooleista vain *tuotannon työnjohtajalla* on tämä tehtävä.) Toimi sitten seuraavasti:

1. Siirry määritettävään laitteeseen ja kirjaudu Microsoft Dynamics 365 Supply Chain Managementiin tuotannon työnjohtajana. (Käytä tiliä, jossa on *Ajanseurannan työjohto* -tehtävä.)
1. Varmista, että määritys on käytettävissä siinä laitteessa, jota ollaan määrittämässä. Jos määritystä ei vielä ole, käytettävissä on oletusmääritys. Lisätietoja laitteen määrityksen määrittämisestä on kohdassa [Tuotannon käyttöliittymän määrittäminen](production-floor-execution-configure.md).
1. Valitse **Tuotannonhallinta \> Tuotannonohjaus \> Tuotantoliittymä**.

    Jos tuotannon käyttöliittymä on jo määritetty vähintään kerran nykyisessä laitteessa, kirjautumissivu avautuu. Muussa tapauksessa avautuu aloitussivu.

1. Valitse joko kirjautumis- tai aloitussivulla **Määritä**.
1. Valitse määritys luettelosta.
1. Valitse **Seuraava**.
1. Valitse vähintään yksi suodatin käytettäväksi nykyisessä laitteessa. Näiden suodattimien avulla voidaan varmistaa, että tarpeelliset työt näytetään laitteessa. Määritä suodatin valitsemalla arvoluettelon avaava suodatintyyppi ja valitse sitten suodatusperusteena käytettävä arvo. Seuraavat suodattimet ovat käytettävissä:

    - **Tuotantoyksikkö** – Tämä suodatin on ylimmän tason suodatin. Sillä viitataan yleensä suureen työalueeseen, jossa on useita resurssiryhmiä ja yksittäisiä resursseja.
    - **Resurssiryhmä** – Tämä on keskitason suodatin. Se viittaa yleensä liittyvien resurssien kokoelmaan rajoitetulla työtilan alueella. Jos valitset ensin **Tuotantoyksikkö**-suodattimen, resurssiryhmäluettelossa on vain kyseisen yksikön ryhmiä. Muussa tapauksessa luettelossa on kaikki käytettävissä olevat resurssiryhmät.
    - **Resurssi** – Tämä on yksityiskohtaisin suodatin. Se viittaa yleensä tiettyyn laitteeseen tai muuhun yksittäiseen resurssiin. Jos valitset ensin **Resurssiryhmä**- ja/tai **Tuotantoyksikkö**-suodattimen, resurssiluettelossa on vain kyseisen ryhmän ja/tai yksikön resursseja. Muussa tapauksessa luettelossa on kaikki käytettävissä resurssit.

1. Valitse **OK**.
1. Kirjautumissivu avautuu ja laite on käyttövalmis.

## <a name="allow-a-worker-to-override-the-default-filters"></a>Oletussuodattimien ohitusmahdollisuuden antaminen työntekijälle

Voit antaa tietyille työntekijöille oikeuden muuttaa suodatinasetuksia missä tahansa heidän käytössään olevassa luettelossa. Jos työntekijällä on tämä oikeus, tuotannon käyttöliittymässä on **Suodatin**-painike **Kaikki työt**- ja **Aktiivinen työ** sivuilla.

> [!NOTE]
> Jos työntekijä vaihtaa suodattimen, uusi suodatin on kaikkien laitteeseen kirjautuvien käyttäjien käytössä siitä lähtien.

Voit antaa työntekijän ohittaa laitteelle määritetyt työn oletussuodattimet seuraavasti:

1. Valitse **Työajan seuranta \> Määritys \> Aikarekisteröinnin työntekijät**.
1. Avaa työntekijän **Aikarekisteröinnin työntekijät** -sivu.
1. Määritä **Aikarekisteröinti**-välilehdessä **Määritä suodattimet** -asetukseksi *Kyllä*.

## <a name="run-the-interface-in-full-screen-mode"></a>Käyttöliittymän suorittaminen koko näytön tilassa

Tuotannon käyttöliittymä suoritetaan usein laitteessa, jota käytetään vain tiettyyn tarkoitukseen. Tämän vuoksi voikin olla järkevää suorittaa liittymä koko näytön tilassa siirtymistoimintoja ja/tai selaimen chromea näyttämättä.

- Supply Chain Managementissa näkyvä siirtymisruutu piilotetaan lisäämällä seuraava teksti URL-osoitteen loppuun selaimen osoiterivillä: `\&limitednav=true`.
- Selaimen osoiterivin voi puolestaan piilottaa käyttämällä selaimen omaa koko näytön tilaa. (Lisätietoja on selaimen ohjeissa.)

Seuraavan kuvan yläosassa näkyy käyttöliittymän oletusulkoasu. Alaosassa näkyy, miltä käyttöliittymä näyttää koko näytön tilassa, kun siirtymisruutu on piilotettu.

![Tavallisen ja koko näytön käyttöliittymän vertailu](media/pfei-full-screen.png "Tavallisen ja koko näytön käyttöliittymän vertailu")

## <a name="extend-the-session-past-12-hours"></a>Istunnon pidentäminen yli 12 tuntia kestäväksi

Tuotannon käyttöliittymä kirjautuu automaattisesti ulos, jos kukaan ei käytä sitä 12 tuntiin. Supply Chain Managementin käyttäjän on sitten kirjauduttava uudelleen sisään. Aikakatkaisurajan voi kuitenkin pidentää enintään 90 päivään.

Aikakatkaisurajaa voi pidentää kirjautumalla Supply Chain Managementiin ja valitsemalla **Järjestelmän hallinta \> Käyttäjät \> Istunnon laajennukset**. Määritä Supply Chain Managementin käyttäjätili, jota käytetään laitteeseen kirjautumiseen, ja kuinka monta tuntia istunto pysyy aktiivisena.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]