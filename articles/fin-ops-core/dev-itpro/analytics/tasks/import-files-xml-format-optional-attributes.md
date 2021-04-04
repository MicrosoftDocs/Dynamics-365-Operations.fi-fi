---
title: (RCS) Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä
description: Tässä ohjeaiheessa on tietoja tavalla, jolla käyttäjä voi suunnitella ER-muodon määrityksen tuomaan tiedostoja valinnaisia määritteitä sisältävän XML-muodon.
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ef090270b2e521b870697bb238b50ea92d4f6958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565683"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä

[!include [banner](../../includes/banner.md)]

Seuraavissa vaiheissa käsitellään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella ER-muotomäärityksen tuomaan valinnaisia määritteitä sisältävän XML-muotoisia tiedostoja. Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista. Ennen kuin aloitat, lataa ja tallenna IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-tiedosto paikallisesti [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).

1.    Valitse **Kaikki työtilat** > **Sähköinen raportointi**.
2.    Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.
3.    Valitse **Raportointikonfiguraatiot**.

## <a name="create-a-new-data-model-configuration"></a>Uuden tietomallin konfiguraation luominen
1.    Avaa valintaikkuna valitsemalla **Luo konfigurointi**.
2.    Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimalli.
3.    Valitse **Luo konfiguraatio**.
4.    Valitse **Suunnittelutoiminto**.
5.    Avaa valintaikkuna valitsemalla **Uusi**.
6.    Kirjoita **Nimi**-kenttään Juuri.
7.    Valitse **Lisää**.
8.    Avaa valintaikkuna valitsemalla **Uusi**.
9.    Kirjoita **Nimi**-kenttään Luettelo.
10.    Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.
11.    Valitse **Lisää**.
12.    Avaa valintaikkuna valitsemalla **Uusi**.
13.    Kirjoita **Nimi**-kenttään Koodi.
14.    Valitse **Nimiketyyppi**-kentässä **Merkkijono**.
15.    Valitse **Lisää**.
16.    Valitse **Tallenna**.
17.    Sulje sivu.
18.    Valitse **Muuta tila**.
19.    Valitse **Valmis**.
20.    Valitse **OK**.

## <a name="create-a-format-for-data-import"></a>Tietojen tuontimuodon luominen
1.    Avaa valintaikkuna valitsemalla **Luo konfigurointi**.
2.    Kirjoita **Uusi**-kenttään Muoto perustuu tietomalliin Xml-tiedoston tuontimalli.
3.    Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimuoto.
4.    Valitse **Tukee tietojen tuontia** -kentässä **Kyllä**.
5.    Valitse **Luo konfiguraatio**.

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>Muodon suunnitteleminen jäsentämään saapuvan tiedosto xml-muodossa
1.    Valitse **Suunnittelutoiminto**.
2.    Avaa valintaikkuna valitsemalla **Lisää juuri**.
3.    Valitse puussa **XML\Elementti**.
4.    Kirjoita **Nimi**-kenttään root.
5.    Valitse **OK**.
6.    Avaa valintaikkuna valitsemalla **Lisää**.
7.    Valitse puussa **XML\Elementti**.
8.    Kirjoita **Nimi**-kenttään document.
9.    Valitse **Monimuotoisuus**-kentässä **Yksi tai useita**.
10.    Valitse **OK**.
11.    Valitse puussa **root\document**.
12.    Avaa valintaikkuna valitsemalla **Lisää**.
13.    Valitse puussa **XML\Määrite**.
14.    Kirjoita **Nimi**-kenttään ID.
15.    Valitse **OK**.
16.    Valitse **Tallenna**.

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>Muodon yhdistämisen suunnitteleminen tallentamaan jäsennetty tieto tietomalliin
1. Valitse **Yhdistä muoto malliin**.
2. Valitse **Uusi**.
3. Anna tai valitse **Määritys**-kentän arvo.
4. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
5. Kirjoita **Nimi**-kenttään Yhdistäminen.
6. Valitse **Tallenna**.
7. Valitse **Suunnittelutoiminto**.
8. Laajenna puussa **format**.
9. Laajenna puussa **format\root: XML Element(root)**.
10.    Valitse puussa **format\root: XML Element(root)\document: XML Element 1..* (tiedosto)**.
11.    Valitse **Sido**.
12.    Laajenna puussa **format\root: XML Element(root)\document: XML Element 1..* (tiedosto)**.
13.    Valitse puussa **format\root: XML Element(root)\document: XML Element 1..* (tiedosto)\id**.
14.    Laajenna puussa **List = format.root.document**.
15.    Valitse puussa **List = format.root.document\Code**.
16.    Valitse **Sido**.
17.    Valitse **Tallenna**.
18.    Sulje sivu.
 
## <a name="run-format-mapping"></a>Muodon yhdistämisen suorittaminen
1. Valitse **Suorita**.
2. Valitse ensin **Selaa** ja sitten **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.
3. Valitse **OK**.

> [!NOTE]
> Valittua tiedostoa ei ole tuotu, sillä muodon rakenne olettaa, että document-elementissä on id-määrite mutta tuodussa tiedostossa tätä määritettä ei ole.

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>Muodon rakenteen muokkaaminen käsittelemään xml-määritettä valinnaisena
1. Sulje sivu.
2. Laajenna puussa **root\document**.
3. Valitse puussa **root\document\id**.
4. Valitse **Puuttuvan määritteen tyhjä merkkijono** -kentässä **Kyllä**.
5. Valitse **Tallenna**.
 
## <a name="run-format-mapping-to-test-changes"></a>Muutosten testaaminen suorittamalla muodon yhdistäminen
1. Valitse **Yhdistä muoto malliin**.
2. Valitse **Suorita**.
3. Valitse ensin **Selaa** ja sitten **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**-tiedosto.
4. Valitse **OK**.
5. Tarkista luotu tiedosto. 

> [!NOTE]
> Sama tiedosto on tuotu, sillä muodon rakenne käsittelee document-elementit id-määritettä nyt valinnaisena.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]