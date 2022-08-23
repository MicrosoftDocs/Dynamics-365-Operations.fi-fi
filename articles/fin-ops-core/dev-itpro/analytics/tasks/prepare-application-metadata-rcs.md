---
title: Sovelluksen metatietojen valmisteleminen RCS:ssä käytettäviksi
description: Tässä artikkelissa käsitellään sovelluksen metatiedot sisältävän uuden raportointimäärityksen luontia.
author: kfend
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: a9ccbb120be43eaf7a8ae8b5bf8eaafb4850b199
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289971"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Sovelluksen metatietojen valmisteleminen RCS:ssä käytettäviksi
[!include [banner](../../includes/banner.md)]

Seuraavat vaiheet selittävät, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli voi luoda uuden sähköisen raportoinnin (ER) konfiguraation. Tämä konfiguraatio sisältää sovelluksen metatiedot ER-mallin yhdistämismääritysten suunnittelemiseen Regulatory Configuration Servicessä (RCS). Tätä konfiguraatiota käytetään sen ER-näytemallin yhdistämismäärityksen suunnittelemiseen, jolla käytetään ulkomaankauppatapahtumia. Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä. Näitä vaiheita varten on ensin suoritettava artikkelissa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.

## <a name="prerequisites"></a>Edellytykset
1.    Valitse **Organisaation hallinto** > **Työtilat** > **Sähköinen raportointi**. 
2.    Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet. 
3.    Valitse **Metatietojen konfiguraatiot**. 
4.    Oletetaan, että RCS:ää käytetään suunnittelemaan sellainen Finance and Operations -sovelluksen ER-ratkaisu, jolla luodaan ulkomaankaupan liiketoimintatoimialueen tietoja sisältäviä sähköisiä asiakirjoja. Jos haluat määrittää ER-tietomallin ja tarvittavien tietojen lähteiden välisen määrityksen, RCS:ssä on oltava Finance and Operations -sovelluksen metatietojen käyttöoikeudet. Tämän vuoksi ER-ratkaisun suunnittelun osana on määritettävä uusi ER-metatietokonfiguraatio, joka sisältää kaikki valitun liiketoimintatoimialueen ER-raporttien luontiin tällä hetkellä tarvittavat metatiedot. 

## <a name="add-metadata-configuration"></a>Metatietojen konfiguroinnin lisääminen 
1.    Avaa valintaikkuna valitsemalla **Luo konfigurointi**. 
2.    Kirjoita **Nimi**-kenttään Ulkomaankaupan yhdistäminen. 
3.    Valitse **Luo konfiguraatio**. 
4.    Valitse **Suunnittelutoiminto**. 
5.    Valitse **Lisää**. 
  
> [!NOTE]
> Voit valita joko koko sovelluksen tai valittujen mallien tai moduulien kaikki metatiedot. Muista kuitenkin, että tässä tapauksessa seuraavat metatiedot lisätään automaattisesti: tietue-, luettelo- ja laajennetut tietotyyppitaulukot. Jos muita metatietoja tarvitaan, ne on lisättävä manuaalisesti. 
 
Ulkomaankauppatapahtumiin liittyvät metatiedot saadaan valitsemalla metatietonimikkeet manuaalisesti. 
  
6.    Valitse **Lisää tietolähde**. 
7.    Valitse **Taulukon tietueet**. 
8.    Voit suodattaa pikasuodattimella **Nimi**-kenttää arvolla Intrastat. 
9.    Valitse **Intrastat**-taulukkotietue. 
10.    Valitse **OK**.
  
Intrastat-taulukkotietueen metatiedot on lisätty. 
  
11.    Laajenna puussa **Taulukkotietueet Intrastat**\>**Suhteet**. 
12.    Valitse puussa **Taulukkotietueet Intrastat**\>**Suhteet\IntrastatCommodity (Taulukkotietueet EcoResCategory)**.     
13.    Valitse **Lisää metatiedot**. 
  
> [!NOTE]
> Valitun taulukkotietueen pakollisten suhteiden metatiedot on lisättävä manuaalisesti. 
  
16.    Valitse **Lisää tietolähde**. 
17.    Valitse **Luettelointi**. 
18.    Voit suodattaa pikasuodattimella **Nimi**-kenttää arvolla IntrastatDirection. 
19.    Valitse **IntrastatDirection-luettelointi**-tietue. 
20.    Valitse **OK**. 
21.    Valitse **Tallenna**.  
22.    Sulje sivu. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Metatietokonfiguraation luonnosversion suorittaminen
1.    Valitse **Muuta tila**. 
2.    Valitse **Valmis**. 
3.    Valitse **OK**. 
4.    Valitse valmis versio **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Metatietokonfiguraation valmiin version vienti sovelluksesta XML-tiedostona
1.    Valitse **Vaihto**. 
2.    Valitse **Vie XML-tiedostona**. 
3.    Valitse **OK**. 
    
Luotu ER-metatietokonfiguraatio on tallennettu XML-tiedostona, joka voidaan tuoda RCS:ään ja jota voidaan käyttää ulkomaankaupan liiketoimintatoimialueen metatietojen tietolähteenä. Näiden tietojen perusteella voidaan määrittää sovelluksen metatietojen ja ER-tietomallin välisen yhdistämismäärityksen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
