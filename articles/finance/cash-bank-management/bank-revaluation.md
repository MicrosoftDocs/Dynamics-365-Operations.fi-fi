---
title: Pankin ulkomaanvaluutan uudelleenarvostus
description: Tämä artikkelissa sisältää yhteenvedon pankin ulkomaanvaluutan uudelleenarvostusprosessista. Se sisältää tietoja asetuksista, prosessin suorittamisesta ja laskemisesta sekä uudelleenarvostustapahtumien peruutuksesta.
author: angelad116
ms.date: 12/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2d5e8a36d3b4d44c9ad0454db94164adebf80997
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887256"
---
# <a name="bank-foreign-currency-revaluation"></a>Pankin ulkomaanvaluutan uudelleenarvostus

[!include [banner](../includes/banner.md)]


Tämä artikkelissa sisältää yhteenvedon pankin ulkomaanvaluutan uudelleenarvostusprosessista. Ohjeaiheessa kerrotaan, miten prosessi määritetään ja suoritetaan. Se sisältää myös tietoja prosessin laskennasta. Ohjeaiheessa kerrotaan, miten uudelleenarvostustapahtumia peruutetaan, jos peruutus vaaditaan.

Kirjanpidon käytännöt edellyttävät kauden lopussa tehtävää pankkitilien ulkomaanvaluutan saldojen uudelleenarvostusta käyttäen eri vaihtokurssityyppejä (esimerkiksi nykyinen, historiallinen ja keskiarvo). Pankin ulkomaanvaluutan uudelleenarvostustoimintoa voi käyttää yhden tai usean pankkitilin uudelleenarvostukseen. Toiminto on myös yleinen toiminto. Tämän vuoksi voit uudelleenarvostaa yksittäiseltä sivulta kaikkien yritysten pankit, joiden käyttöoikeus sinulla on.

> [!NOTE]
> Uudelleenarvostusprosessia suoritettaessa kunkin pankkitilin ulkomaanvaluuttana kirjattu saldo uudelleenarvostetaan. Uudelleenarvostusprosessin aikana luodut toteutumaton voitto- tai tappiotransaktiot ovat järjestelmän luomia. Voidaan luoda kaksi tapahtumaa, joista yksi on kirjanpitovaluuttaa ja toinen raportointikurssin valuuttaa varten, jos raportointivaluutta kuuluu asiaan. Jokainen kirjanpitomerkintä kirjataan toteutumattomaan voittoon tai tappioon ja päätilille, joka uudelleenarvostetaan.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen suorittamisen valmisteleminen

Seuraavat asetukset on määritettävä ennen uudelleenarvostusprosessin suorittamista.

- Määritä vaihtokurssin tyyppi **Kirjanpito**-sivulla. Jos päätilin vaihtokurssin tyyppiä ei ole määritetty, tätä vaihtokurssia käytetään ulkomaanvaluutan uudelleenarvostuksen yhteydessä.
- Määritä **Kirjanpito**-sivulla valuutan uudelleenarvostuksen toteutuneen voiton, toteutuneen tappion, toteutumattoman voiton ja toteutumattoman tappion tilit. Toteutuneen voiton ja tappion tilejä käytetään, kun myyntireskontran ja ostoreskontran tapahtumat selvitetään. Toteutumattoman voiton ja tappion tilejä käytetään avointen tapahtumien ja kirjanpidon päätilien uudelleenarvostuksessa.
- Valitse **Valuutan uudelleenarvostustilit** -sivulla kullekin valuutalle ja yritykselle eri valuutan uudelleenarvostustilit. Jos tilejä ei ole määritetty, käytetään **Kirjanpito**-sivun tilejä.
- Lisää numerojärjestys ulkomaanvaluutan uudelleenarvostukseen **Maksuliikennetiedot**-sivun **Numerojärjestykset**-välilehdessä.


> [!NOTE]
> Jos yrityksessä käytetään Venäjän, Puolan tai Unkarin maa- tai aluekoodia, voit jo tehdä pankin ulkomaanvaluutan uudelleenarvostuksen. Et voi käyttää ulkomaanvaluutan uudelleenarvostusta, joka on käytössä muissa maissa tai muilla alueilla.

## <a name="process-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen käsittely

Kun asennus on valmis, voit uudelleenarvostaa yhden tai usean pankkitilin saldot kaikissa yrityksissä maksuliikenteen hallinnan **Ulkomaanvaluutan uudelleenarvostus** -sivun avulla. Voit suorittaa prosessin reaaliaikaisena tai ajoittaa sen erän avulla.

**Ulkomaanvaluutan uudelleenarvostus** -sivu sisältää kunkin uudelleenarvostusprosessin historian. Sivulla ovat tiedot prosessin suoritusajankohdasta ja käytetyistä ehdoista. Sivulla on myös linkki uudelleenarvostuksesta luotuun tositteeseen. Sivu sisältää myös tiedon siitä, onko edellinen uudelleenarvostus peruutettu. Voit suorittaa uudelleenarvostusprosessin valitsemalla **Ulkomaanvaluutan uudelleenarvostus** -kohdan toimintoruudussa ja avaamalla **Pankki - ulkomaanvaluutan uudelleenarvostus** -valintaikkunan.

**Uudelleenarvostuksen päivämäärä** -kenttä määrittää uudelleenarvostettavan ulkomaanvaluutan saldon laskennan katkaisupäivämäärän. Kaikkien tähän päivämäärään mennessä tapahtuneiden pankkitapahtumien summa, joka arvostetaan uudelleen.

**Vaihtokurssin päivämäärä** -kenttä määrittää sen vaihtokurssin päivämäärän, jota käytetään valuuttasaldojen uudelleenarvostuksessa. Voit uudelleenarvostaa esimerkiksi saldot 31.1., mutta käyttää vaihtokurssia, joka on määritetty päivämäärälle 1.2.

Uudelleenarvostusprosessi voidaan suorittaa vähintään yhdelle oikeushenkilölle. Haussa näkyvät vain ne yritykset, joiden käyttöoikeus sinulla on. Valitse yritykset, joille haluat valita sellaiset pankkitilit, joissa ulkomaanvaluutan uudelleenarvostus on käytössä. Kaikki näiden yritysten pankkitilit näkyvät ruudukossa.

Määritä **Esikatsele ennen kirjausta** -vaihtoehdon arvoksi **Kyllä**, jos haluat tarkastella uudelleenarvostuksen tuloksia ennen niiden julkaisemista. Ulkomaanvaluutan uudelleenarvostuksella on esikatselu, jonka voi julkaista. Sinun ei tarvitse suorittaa uudelleenarvostusprosessia uudelleen. Voit viedä esikatselun tulokset Microsoft Exceliin ja näin säilyttää tiedot siitä, miten summat on laskettu. Et voi käyttää eräkäsittelyä, jos haluat esikatsella uudelleenarvostuksen tuloksia.

Valitse **OK**, jos haluat käsitellä ulkomaanvaluutan uudelleenarvostuksen. Kunkin suorituksen historian seuraamista varten luodaan tietue. Kullekin juridiselle henkilölle ja kirjanpitotasolle luodaan erillinen tietue.

## <a name="calculate-unrealized-gainloss"></a>Laske toteutumaton voitto/tappio

Maksuliikenteen hallinnassa pankin valuuttaa pidetään perusvaluuttana. Sitä ei uudelleenarvosteta. Pankkitilin saldo kirjanpitovaluutassa arvostetaan uudelleen käyttämällä pankin valuutan ja kirjanpitovaluutan välisiä vaihtokursseja **vaihtokurssin päivämääränä**. Pankkitilin saldo raportointivaluutassa arvostetaan myös uudelleen käyttämällä pankin valuutan ja raportointivaluutan välisiä vaihtokursseja **vaihtokurssin päivämääränä**.

Pankkitilin ja uuden kirjanpitovaluutassa lasketun saldon väliselle erolle luodaan tapahtuma. Pankkitilin ja uuden raportointivaluutassa lasketun saldon väliselle erolle luodaan toinen tapahtuma. Näiden tapahtumien merkinnät merkitään täsmäytetyiksi. 

Kirjanpitovaluutalle ei tehdä merkintää, jos pankin valuutta vastaa kirjanpitovaluuttaa. Samoin raportointivaluutalle ei tehdä merkintää, jos pankin valuutta vastaa raportointivaluuttaa.

Ulkomaanvaluutan uudelleenarvostustapahtuma jaetaan myös eri dimensioille, jotka löytyvät pankkitapahtumista. Jako perustuu kunkin dimension saldoon. Tässä esimerkissä pankin kokonaissaldo on 10 000, mutta liiketoimintayksikön 001 saldo on 4 000 ja liiketoimintayksikön 002 saldo on 6 000. Tässä tapauksessa 40 prosenttia uudelleenarvostuksen summasta kirjataan uudelleenarvostustilille, jolla on liiketoimintayksikkö 001, ja 60 prosenttia kirjataan uudelleenarvostustilille, jolla on liiketoimintayksikkö 002. Jos tilirakenne ei sisällä liiketoimintayksikköä, koko summa kirjataan uudelleenarvostustilille.

## <a name="reverse-foreign-currency-revaluation"></a>Käänteinen ulkomaanvaluutan uudelleenarvostus

Jos uudelleenarvostustapahtuma pitää palauttaa, valitse **Ulkomaanvaluutan uudelleenarvostus** -sivun **Palautustapahtuma**. Uusi ulkomaanvaluutan uudelleenarvostuksen historiatietue luodaan ylläpitämään historian kirjausketjua ulkomaanvaluutan uudelleenarvioinnin ajankohdasta tai palautuksesta.

Jos haluat peruuttaa useita uudelleenarvostuksia, peruuta ensin uusin uudelleenarvostus. Jatka sitten vanhempien uudelleenarvostusten peruutusta päivämäärän osoittamassa järjestyksessä. Tämän jälkeen voit käsitellä uudet uudelleenarvostukset peruutetuilta kausilta.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
