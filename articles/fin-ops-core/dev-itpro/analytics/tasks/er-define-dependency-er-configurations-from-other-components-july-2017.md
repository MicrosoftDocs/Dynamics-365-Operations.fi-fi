---
title: Sähköisen raportoinnin konfiguraatioiden riippuvuuden määrittäminen muissa komponenteissa
description: Tässä artikkelissa käsitellään sähköisen raportoinnin (ER) määrityksen suunnittelua ja sen riippuvuuden määrittämistä muista ohjelmisto-osista.
author: kfend
ms.date: 07/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff9d1edab13de49ae676708865ebe02a82db34e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291261"
---
# <a name="define-the-dependency-of-er-configurations-on-other-components"></a>Sähköisen raportoinnin konfiguraatioiden riippuvuuden määrittäminen muissa komponenteissa

[!include [banner](../../includes/banner.md)]

Voit suorittaa nämä vaiheet, jos ER Mallin yhdistämismäärityksen konfiguraatioiden hallinta -tehtäväoppaan vaiheet on suoritettu ja sinulla on Microsoft Dynamics Lifecycle Services (LCS) -palvelun käyttöoikeus.

Tässä menettelyssä kerrotaan, miten sähköisen raportoinnin (ER) konfiguraatio suunnitellaan ja miten sen riippuvuus muista ohjelmistojen komponenteista määritetään. Näin voit varmistaa, että konfiguraatio ladataan oikein tiettyyn talous- ja toimintosovellusten versioon. Tässä esimerkissä luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware, Inc. 

Nämä ohjeet on tarkoitettu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska yritykset jakavat ER-konfiguraatiot. 

1. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
    * Varmista, että konfiguraatioiden puurakenne sisältää Tietomallin esimerkki -konfiguraation ja alinimikkeet. Suorita muussa tapauksessa ER Mallin yhdistämismäärityksen konfiguraatioiden hallinta -tehtäväoppaan vaiheet. Aloita sitten tämä opas uudelleen.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>ER-konfiguraatioiden riippuvuuden määrittäminen muista osista
1. Laajenna puussa Sample data model.
2. Valitse puussa Sample data model\Sample mapping.
    * Valitaan Esimerkkiyhdistämismääritys-mallin yhdistämismäärityksen konfiguraation luonnosversio. Nyt määritetään sen riippuvuus muista ohjelmistokomponenteista. Tämä vaihe on edellytys tämän konfiguraation version sähköisen raportoinnin säilöstä latauksen hallinnan ja muiden tämän version käyttötarkoitusten edellytys.   
3. Laajenna Edellytykset-osa.
    * Huomaa, että toteutusten edellytysten ryhmä on lisätty automaattisesti tässä vaiheessa. Tämä ryhmä sisältää edellytetyn komponentin, joka viittaa tietomallin konfiguraatioon. Sen Toteutus-merkintä on käytössä. Merkintä tarkoittaa, että Esimerkkiyhdistämismääritys-yhdistämismäärityksen konfiguraatiota pidetään Tietomallin esimerkki -tietomallin toteutuksena. Tämä komponentti pakottaa sähköisen raportoinnin lataamaan Esimerkkiyhdistämismääritys-yhdistämismäärityksen konfiguraation sähköisen raportoinnin säilöstä aina, kun Tietomallin esimerkki -mallin konfiguraatio ladataan.   
4. Valitse Muokkaa.
    * Konfiguraation nykyisen version yksittäinen riippuvuus ohjelmiston komponentista voidaan määrittää käyttämällä komponentin tyypin määritelmää ja joko komponentin versiota tai komponentin versioiden aluetta.  
    * Halutut riippuvuudet voidaan ryhmitellä yhteen. Kun ryhmittelyn tyypiksi valitaan Kaikki, ryhmän riippuvuuden ehdon katsotaan täyttyneen, kun kukin tämän ryhmän ja aliryhmän riippuvuuden ehto täyttyy. Kun ryhmittelyn tyypiksi valitaan Yksi seuraavista, ryhmän riippuvuuden ehdon katsotaan täyttyneen, kun vähintään yksi tämän ryhmän riippuvuuden ehto täyttyy.   
5. Valitse Uusi.
6. Valitse Tuotteen edellytetty komponentti.
7. Valitse Microsoft Dynamics 365 for Operations (1611).
8. Kirjoita Versio-kenttään [7.1.1541.3036,8).
    * [7.1.1541.3036,8)  
    * Annetut riippuvuudet arvioidaan, kun tämä konfiguraatio ladataan mistä tahansa sähköisen raportoinnin säilöstä. Tämä konfiguraation versio ladataan sähköisen raportoinnin säilöstä, kun Tietomallin esimerkki -konfiguraation versio 1 on jo paikallaan tai ladattu etukäteen. Jos se on ladattu etukäteen, se on tehtävä valmiiksi talous- ja toimintosovellusten versiossa 7.1.1541.3036 tai uudemmassa. Versio ei kuitenkaan saa olla uudempi kuin pääversio 8.   
9. Valitse Tallenna.
10. Sulje sivu.
11. Voit muuttaa tilaa valitsemalla Muuta.
12. Valitse Valmis.
13. Valitse OK.
14. Valitse puussa Sample data model\Sample mapping (alternative).
15. Valitse Muokkaa.
16. Valitse Uusi.
17. Valitse Tuotteen edellytetty komponentti.
18. Valitse Microsoft Dynamics AX 7.0 RTW.
19. Kirjoita Versio-kenttään [7.0.1265.3015,7.1).
    * [7.0.1265.3015,7.1)  
    * Riippuvuudet arvioidaan, kun tämä konfiguraatio ladataan mistä tahansa sähköisen raportoinnin säilöstä. Tämä konfiguraation versio ladataan sähköisen raportoinnin säilöstä, kun Tietomallin esimerkki -konfiguraation versio 1 on jo paikallaan tai ladattu etukäteen. Jos se on ladattu etukäteen, se on tehtävä valmiiksi Microsoft Dynamics 365 Financessa, Enterprise editionissa, jonka version on oltava 7.0.1265.3015 tai uudempi. Versio ei kuitenkaan saa olla uudempi kuin aliversio 1.   
20. Valitse Tallenna.
21. Sulje sivu.
22. Voit muuttaa tilaa valitsemalla Muuta.
23. Valitse Valmis.
24. Valitse OK.

## <a name="configure-the-er-repository"></a>ER-säilön määrittäminen
1. Sulje sivu.
2. Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.
    * Avaa nykyisen sähköisen raportointipalvelun Litware Inc. -yrityksen sähköisen raportoinnin säilöt.  
3. Merkitse valittu rivi luettelossa.
4. Valitse Säilöt.
5. Valitse Näytä suodattimet.
6. Syötä Tyypin nimi -kenttään suodattimen LCS-arvo käyttämällä sisältää-suodatinoperaattoria.
    * Jos LCS-säilö on jo rekisteröity nykyisessä sähköisessä raportointipalvelussa, voit ohittaa tämän alitehtävän jäljellä olevat vaiheet. Jos LCS-säilöä ei ole vielä rekisteröity, suorita jäljellä olevat vaiheet.   
7. Avaa valintaikkuna valitsemalla Lisää.
8. Syötä Konfiguraatiosäilön tyyppi -kentän arvoksi LCS.
9. Valitse Luo säilö.
10. Anna tai valitse Projekti-kentässä arvo.
    * Valitse haluamasi LCS-projekti Projekti-kentän hausta.  
11. Valitse OK.
12. Sulje sivu.

## <a name="upload-configurations-to-lcs"></a>Konfiguraatioiden lataaminen LCS:ään
1. Valitse Raportointikonfiguraatiot.
2. Valitse puussa Sample data model.
3. Valitse tämän konfiguraation valmis versio.
4. Voit muuttaa tilaa valitsemalla Muuta.
5. Valitse Jaa.
6. Valitse OK.
    * Tämän mallin konfiguraation versio 1 on ladattu LCS:ään LCS-projektin avulla aiemmin määritetyn sähköisen raportoinnin säilöä varten.   
7. Laajenna puussa Sample data model.
8. Valitse puussa Sample data model\Sample mapping.
9. Valitse tämän konfiguraation valmis versio.
10. Voit muuttaa tilaa valitsemalla Muuta.
11. Valitse Jaa.
12. Valitse OK.
    * Tämän mallin yhdistämismäärityksen konfiguraation versio 1.1 on ladattu LCS:ään LCS-projektin avulla aiemmin määritetyn sähköisen raportoinnin säilöä varten.   
13. Valitse puussa Sample data model\Sample mapping (alternative).
14. Valitse tämän konfiguraation valmis versio.
15. Voit muuttaa tilaa valitsemalla Muuta.
16. Valitse Jaa.
17. Valitse OK.
    * Tämän mallin yhdistämismäärityksen konfiguraation versio 1.1 on ladattu LCS:ään LCS-projektin avulla aiemmin määritetyn sähköisen raportoinnin säilöä varten.   

## <a name="evaluate-er-configuration-dependencies"></a>ER-konfiguraation riippuvuuksien arvioiminen
Luodut konfiguraatiot poistetaan järjestelmästä ja ladataan takaisin LCS-säilöstä.  
1. Valitse puussa Sample data model\Sample mapping.
2. Valitse Poista.
3. Valitse Kyllä.
4. Valitse puussa Sample data model\Sample mapping (alternative).
5. Valitse Poista.
6. Valitse Kyllä.
7. Valitse puussa Sample data model\Sample format.
8. Valitse Poista.
9. Valitse Kyllä.
10. Valitse puussa Sample data model.
11. Valitse Poista.
12. Valitse Kyllä.
13. Sulje sivu.
    * Avaa nykyisen sähköisen raportointipalvelun Litware Inc. -yrityksen sähköisen raportoinnin säilöt.  
14. Valitse Säilöt.
15. Valitse Näytä suodattimet.
16. Syötä Tyypin nimi -kenttään suodattimen LCS-arvo käyttämällä sisältää-suodatinoperaattoria.
17. Valitse Avaa.
18. Valitse puussa Sample data model.
    * Ota huomioon, että voit tarkastella arviointia edellytysehtojen täyttymisestä nykyisen säilön kunkin ER-konfiguraation kohdalla. Voit tarkastella tätä arvioinnissa valitsemalla Tarkista edellytykset.   
19. Valitse Tarkista edellytykset.
20. Valitse Tuo.
21. Valitse Kyllä.
22. Sulje sivu.
23. Sulje sivu.
24. Sulje sivu.
25. Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.
26. Laajenna puussa Sample data model.
    * Huomaa, että Esimerkkiyhdistämismääritys-mallin yhdistämismäärityksen konfiguraatio on ladattu yhdessä valitun tietomallin konfiguraation kanssa. Nämä kaksi tiedostoa ladataan yhdessä, koska Esimerkkiyhdistämismääritys-konfiguraatio on määritetty valitun tietomallin toteutuksessa. Se on myös käytössä sovelluksessa. Esimerkkiyhdistämismääritys (vaihtoehto) -konfiguraatiota ei ladattu, koska pakollisen sovellusversion ehtoja ei täytetä.   
    * Jos kirjaudut sisään talous- ja toimintosovelluksiin, rekisteröit saman tarjoajan, käytät samaa LCS-projektia ja lataat saman tietomallin konfiguraation, Esimerkkiyhdistämismääritys (vaihtoehto) -konfiguraatio ladataan, kun taas Esimerkkiyhdistämismääritys-konfiguraatio ohitetaan.  

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) määritysten elinkaaren hallinta](../general-electronic-reporting-manage-configuration-lifecycle.md)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

