---
title: Toimittajan maksun yleiskatsaus
description: Tässä tehtävän ohjauksessa kerrotaan toimittajan maksujen luomisessa käytettävistä eri tavoista. Niitä ovat esimerkiksi maksuehdotuksen käyttäminen ja kertaluontoisen maksun syöttäminen.
author: kweekley
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4402be4be52f71bf346a1f85155aad4b9890b3bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827287"
---
# <a name="vendor-payment-overview"></a>Toimittajan maksun yleiskatsaus

[!include [banner](../../includes/banner.md)]

Tässä tehtävän ohjauksessa kerrotaan toimittajan maksujen luomisessa käytettävistä eri tavoista. Niitä ovat esimerkiksi maksuehdotuksen käyttäminen ja kertaluontoisen maksun syöttäminen. Näissä toimintaohjeissa käytetään esittely-yritystä USMF.

1. Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra > Maksut > Maksukirjauskansio**.
2. Valitse **Uusi**.
3. Valitse maksukirjauskansio, jonne toimittajan maksut tallennetaan. 
4. Valitse kirjauskansio tai syötä se manuaalisesti.
5. Valitse **Rivit**.
6. Valitse **Toimintoruutu**-osiosta **Maksuehdotus**.
7. Valitse **Luo maksuehdotus**. Maksuehdotus on kysely, jota käytetään maksun laskujen valitsemisessa. Voit muokata maksettavien laskujen luetteloa ennen toimittajan maksujen luomista.
8. Valitse laskut maksua varten eräpäivän, käteisalennuksen tai molempien avulla. 
9. Syötä päivämäärä eräpäivän tai käteisalennuksen vertailua varten. 
10. Valinnainen: Syötä kaikissa maksuissa käytettävä maksupäivämäärä. Tähän syötetty päivämäärä on kaikkien luotujen maksujen maksupäivä eräpäivästä tai käteisalennuksen päivästä riippumatta.  
11. Valinnainen: Syötä aikaisin mahdollinen maksupäivä. Aikaisin maksupäivä on aikaisin päivä, jolloin maksuja luotiin. Jos esimerkiksi laskun eräpäivä on aikaisimman maksupäivän jälkeen, eräpäiväksi tulee maksupäivä aikaisimman maksupäivän sijaan, jotta laskun voi maksaa mahdollisimman myöhään.
12. Syötä **Sisällytettävät tietueet** -osioon kyselyn lisärajoitukset. Suodattimen avulla voi rajata maksua varten valittuja laskuja toimittajaryhmän tai maksutavan perusteella. Voit lisätä esimerkiksi suodattimen, jos haluat maksaa laskut vain sekkimaksuna tässä maksuajossa.
13. Syötä kyselyn lisärajoitukset tai maksun oletusarvot. Lisäparametrien avulla voi määrittää maksun valuutan tai tämän maksuajon keskitetyt maksut.  
14. Valitse **OK**. Kun olet valinnut **OK**, näkyviin tulevat kyselyn tulokset. Jos et halua esikatsella maksettavien laskujen luetteloa, voit siirtyä takaisin **Parametrit**-pikavälilehteen ja muuttaa **Luo maksut ilman laskun esikatselua** -asetukseksi Kyllä.  
15. Valitse **Näytä maksun yleiskatsaus** -painike, kun haluat tarkastella toimittajalle valitusta laskusta luotavia maksuja.
16. Valitse **Piilota maksun yleiskatsaus** -painike piilottaaksesi maksut. 
17. Valitse **Luo maksut**. Ennen kuin valitset **Luo maksut**, voit napsauttaa ruudukkoa hiiren kakkospainikkeella ja tuoda laskuluettelon Exceliin. **Luo maksut** -painike luo toimittajan maksut maksukirjauskansioon.  
18. Skannaa maksut ja varmista, että kaikille maksuille on määritetty maksutapa. Jos luotavana on maksuja, kuten sekin tulostaminen tai sähköisen maksun luominen, maksutapa on määritettävä. Maksutavan oletusarvo saadaan pankkitilistä, jolle maksu tehdään.  
19. Luo kertaluonteinen maksu valitsemalla **Uusi**. Kertaluonteinen maksu voidaan lisätä maksukirjauskansioon milloin tahansa ennen kirjaamista. Tämä tehdään valitsemalla **Uusi**-painike ja lisäämällä maksun tiedot manuaalisesti mieluummin kuin **Maksuehdotus**-vaihtoehdon avulla.  
20. Valitse toimittaja, jolle maksu tehdään.
21. Jos maksettava lasku on olemassa, valitse maksun lasku valitsemalla **Selvitä tapahtumat** -kohta. Jos tämä on ennakkomaksu, vaihe on valinnainen. Voit luoda maksun valitsemalla ainoatakaan laskua. 
22. Merkitse kaikki maksettavat laskut. Jos valitset maksun laskut **Selvitä tapahtumat** -kohdan avulla, maksusumma lasketaan automaattisesti maksua varten merkittyjen laskujen ja **Täsmäytettävä summa** -kohtaan syötetyn summan perusteella.
23. Valitse **OK**.
24. Jos haluat poistaa maksun, merkitse rivi.
25. Valitse **Poista**. Maksun poistaminen poistaa vain maksun. Maksua varten merkityt laskut ovat yhä käytettävissä toisessa maksussa maksamista varten.
26. Valitse **Kyllä**.
27. Valitse **Luo maksu** tulostaaksesi sekkejä tai luodaksesi sähköisen maksutiedoston.
28. Valitse luotava maksutapa. Maksukirjauskansio voi sisältää sekä sekkimaksuja että sähköisiä maksuja. Siellä voi kuitenkin luoda vain yhden maksutyypin kerralla.
29. Valitse pankkitili, jolta maksut luodaan.
30. Valitse **OK**. Maksut luodaan vain maksuille, jotka vastaavat valitsemiasi **Maksutapa**- ja **Pankkitili**-vaihtoehtoja.
31. Jos olet luomassa **sekkejä**, valitse **Asiakirja** varmistaaksesi, että sekeille valitaan oikea tulostuskohde.
32. Valitse **OK**.
33. Luo maksut valitsemalla **OK**.
34. Valitse **Kirjaa**, jos kaikki maksut on hyväksytty ja luotu. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]