---
title: Käyttöomaisuuden määrittäminen
description: Tämä artikkeli sisältää käyttöomaisuusmoduulin asetusten yleiskatsauksen.
author: moaamer
ms.date: 06/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: kfend
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3baa842dadddd0f763f803528d322b9561b3141e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910139"
---
# <a name="set-up-fixed-assets"></a>Käyttöomaisuuden määrittäminen

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää **käyttöomaisuusmoduulin** asetusten yleiskatsauksen. 

Parametrit hallitsevat käyttöomaisuuden yleisiä toimintoja. Käyttöomaisuusryhmien avulla ryhmitellään käyttöomaisuus ja määritetään kunkin ryhmään liitetyn käyttöomaisuuden oletusmääritteet. Kirjat liitetään käyttöomaisuusryhmiin. Kirjat seuraavat käyttöomaisuuden kirjanpidollista arvoa tiettynä ajanjaksona poistoprofiilissa määritetyn poiston konfiguroinnin avulla.

Käyttöomaisuus liitetään ryhmään luomisen yhteydessä. Käyttöomaisuusryhmiin määritetyt kirjat liitetään tämän jälkeen oletusarvoisesti käyttöomaisuuteen. Kirjat, jotka konfiguroidaan kirjaamaan kirjanpitoon, liitetään kirjausprofiiliin. Kirjanpitotilit määritetään kullekin kirjausprofiilin kirjalle ja niitä käytetään, kun käyttöomaisuustapahtumia kirjataan.

![Käyttöomaisuuskomponentit.](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Poistoprofiilit

Poistoprofiilit on määritettävä ensimmäiseksi. Poistoprofiilissa määritetään, miten käyttöomaisuuserän arvo poistetaan ajan kuluessa. Määritä poistomenetelmä, poistovuosi (kalenterivuosi tai tilikausi) ja poistotiheys. Lisätietoja on kohdassa [Poistoprofiilien luominen ja tarkasteleminen](tasks/set-up-depreciation-profiles.md).

## <a name="books"></a>Kirjat

Kun olet määrittänyt poistoprofiilit, sinun on luotava käyttöomaisuuden edellyttämät kirjat. Jokaisessa kirjassa jäljitetään käyttöomaisuuserän itsenäinen taloudellinen elinkaari. Kirjat voidaan määrittää kirjaamaan liittyvät tapahtumat kirjanpitoon. Tämä määritys on oletusasetus, koska sitä käytetään yleensä yrityksen taloushallinnon raportoinnissa. Kirjat, joita ei kirjata kirjanpitoon, kirjataan vain käyttöomaisuuserän alareskontraan ja käytetään yleensä veroilmoitusta varten.

Ensisijainen poistoprofiili liitetään jokaiseen kirjaan. Kirjoilla on myös vaihtoehtoinen poistoprofiili tai lisäpoistoprofiili, jos tämä profiilityyppi on käytettävissä. Jotta käyttöomaisuuskirja sisällytetään automaattisesti poiston suoritukseen, on otettava käyttöön **Laske poisto** -vaihtoehto. Jos tätä vaihtoehtoa ei ole otettu käyttöön käyttöomaisuuserälle, poistoehdotus ohittaa käyttöomaisuuden.

Voit määrittää myös johdettuja kirjoja. Määritetyt johdetut tapahtumat kirjataan ensisijaisen tapahtuman täydellisenä kopiona johdettuihin kirjoihin. Tämän vuoksi johdetut tapahtumat yleensä määritetään hankinnoille ja luovutuksille eikä poistotapahtumille. Lisätietoja on kohdassa [Arvomallien määrittäminen](tasks/set-up-value-models.md).

**Käyttöomaisuusparametrit**-sivulla voit asetuksen avulla ottaa lukitustoiminnon käyttöön tai poistaa sen käytöstä. Voit ottaa tämän toiminnon käyttöön **Toimintojen hallinta** -työtilassa.

## <a name="fixed-asset-posting-profiles"></a>Käyttöomaisuuserän kirjausprofiili

Kun kirja on määritetty, voit luoda kirjausprofiilin. Kirjausprofiili on määritettävä kirjakohtaisesti, mutta sen voi määrittää myös yksityiskohtaisemmalla tasolla. Voit määrittää esimerkiksi kirjan ja käyttöomaisuusryhmään tai jopa yksittäisten käyttöomaisuuskirjan kirjausprofiilin. Määritettyjä kirjanpitotilejä käytettään oletusarvoisesti käyttöomaisuustapahtumille.

Sinun pitää määrittää kirjanpitotilit, joita käytetään poistoprosessien, eli poistomyynnin ja poistohävikin, aikana. Aiemmin kirjatut käyttöomaisuustapahtumat palautetaan luovutusajankohtana alkuperäisiltä tileiltä. Nettosummat siirretään sitten soveltuvalle tilille käyttöomaisuuden luovutuksen voittoja ja tappioita varten. Jotta tapahtumien palautus tapahtuu oikein, kaikille liiketoiminnassa käytettäville tapahtumatyypeille on määritettävä tilit. Päätilin on oltava kirjausprofiilissa asetetun tapahtumatyypin alkuperäinen tili. Vastatilin tulee olla käyttöomaisuuden poistotilinä käytettävä tulostili. Poikkeus on nettokirjanpitoarvo. Tässä tapauksessa päätili ja vastatili on määritettävä käyttöomaisuuden poistotilinä käytettäväksi tulostiliksi. Lisätietoja on kohdassa [Käyttöomaisuuden kirjausprofiilien määrittäminen](tasks/set-up-fixed-asset-posting-profiles.md).

## <a name="fixed-asset-groups"></a>Käyttöomaisuusryhmät

**Käyttöomaisuusryhmä**-kenttä on ainoa pakollinen kenttä, kun käyttöomaisuus luodaan. Tämän kentän arvo määrittää useita käyttöomaisuuden tietokentän oletusarvon. Kirjat määritetään siten, että jokaiselle omaisuuserän käyttöomaisuudelle on määritetty oletusarvoinen kirja. Tällä tavoin kirjoille määritettävät määritteet ovat käyttöoikeusryhmäkohtaisia. Nämä määritteet sisältävät käyttöiän ja poistomenetelmän.

Voit määrittää myös tietyn käyttöomaisuusryhmän ja kirjan yhdistelmän erityiset poistovähennykset tai bonuspoiston. Erityisen poistovähennyksen prioriteetti määritetään, jotta kirjaan liitettyjen useiden vähennysten laskentajärjestys voidaan määrittää. Lisätietoja on kohdassa [Käyttöomaisuusryhmien määrittäminen](tasks/set-up-fixed-asset-groups.md).

## <a name="journal-names"></a>Kirjauskansioiden nimet

Luo **Kirjauskansioiden nimet** -sivulla käyttöomaisuuden kirjauskansion kanssa käytettävien kirjauskansioiden nimet. Määritä **Kirjauskansion tyyppi** -kentän arvoksi **Kirjaa käyttöomaisuus**. Määritä **Tositesarja**-kenttä siten, että kirjauskansion nimiä käytetään käyttöomaisuuden kirjauskansiossa. Käyttöomaisuuden kirjauskansioissa ei saa käyttää **Vain yksi tositenumero** -asetusta, sillä useissa automatisoiduissa prosesseissa, kuten siirroissa ja jaoissa, on käytettävä yksilöivää tositenumeroa.

## <a name="fixed-asset-parameters"></a>Käyttöomaisuuserien parametrit

Viimeinen vaihe on käyttöomaisuusparametrien päivittäminen.

**Aktivointiraja**-kentässä määritetään poistetut käyttöomaisuuserät. Jos tilausrivejä on valittu käyttöomaisuuseräksi, mutta se ei vastaa määritettyä aktivointirajaa, käyttöomaisuuserä luodaan tai päivitetään, mutta **Laske poisto** -asetukseksi on määritetty **Ei**. Siksi käyttöomaisuutta ei poisteta automaattisesti poistoehdotusten osana.

Tärkeä vaihtoehto on **Luo poisto-oikaisusummat automaattisesti käytöstä poistamisten kanssa**. Jos määrität tämän asetuksen arvoksi **Kyllä**, toiminto oikaisee käyttöomaisuuserän poiston automaattisesti käyttöomaisuuden poiston aikaisten poistoasetusten perusteella. Myös käteisalennukset voidaan vähentää hankintasummasta käyttöomaisuuserien hankinnan yhteydessä toimittajan laskun avulla.

**Lukitse käyttöomaisuuskirjat poistokirjauskansiossa** -parametrin avulla voit lukita käyttöomaisuuskirjat poistokirjauskansiossa. Kun poistotapahtumia kirjataan, järjestelmä tarkistaa, että samaa käyttöomaisuuskirjaa ei ole lisätty useampaan kuin yhteen poistokirjauskansioon. Jos se on lisätty useampaan, käyttöomaisuuskirja lukitaan ja kirjaaminen pysähtyy. Jos käyttöomaisuuskirjan tunnus on lukitussa kirjauskansiossa, sen lukitus poistetaan automaattisesti, kun alkuperäisen kirjauskansion kirjaaminen on valmis. Voit poistaa kirjauskansion lukituksen myös manuaalisesti. 

**Ostotilaukset**-pikavälilehdessä voidaan määrittää, miten käyttöomaisuuserät luodaan ostoprosessin osana. Ensimmäinen vaihtoehto on **Salli käyttöomaisuuden hankinta ostosta**. Jos määrität tämän asetuksen arvoksi **Kyllä** hankinta kirjataan käyttöomaisuuserälle laskun kirjaamisen yhteydessä. Jos määrität tämän asetuksen arvoksi **ei**, käyttöomaisuus voidaan silti asettaa ostotilaukseen ja laskuun, mutta hankintaa ei kirjata. Se tehdään erillisessä vaiheessa käyttöomaisuuden kirjauskansiosta. **Luo käyttöomaisuus tuotteen vastaanoton tai laskun kirjaamisen aikana** -vaihtoehdolla voi luoda uusia varoja kirjauksen aikana. Tämän vuoksi varoja ei tarvitse määrittää käyttöomaisuudeksi ennen tapahtumaa. Viimeinen vaihtoehto **Tarkista käyttöomaisuuden luonti rivimäärityksen aikana** -asetus on käytettävissä vain ostoehdotuksissa.

Syykoodit voidaan konfiguroida niin, että ne ovat pakollisia käyttöomaisuuden muutoksissa tai tietyissä käyttöomaisuustapahtumissa.

**Numerosarjat**-välilehdessä määritetään lopuksi käyttöomaisuuden numerosarjat. Jos **käyttöomaisuusryhmän** numerosarja on määritetty, se voi ohittaa **käyttöomaisuuden** numerosarjan.

Lisätietoja on kohdassa [Käyttöomaisuuden luominen](tasks/create-fixed-asset.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
