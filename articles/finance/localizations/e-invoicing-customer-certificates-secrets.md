---
title: Asiakkaan varmenteet ja salaiset koodit
description: Tässä artikkelissa selitetään, miten asiakkaan varmenteet ja salaiset koodit määritetään sähköisessä laskutuksessa.
author: dkalyuzh
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a4d33135bf352a4c4a245e597e0c3c7467317864
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880657"
---
# <a name="customer-certificates-and-secrets"></a>Asiakkaan varmenteet ja salaiset koodit

[!include [banner](../includes/banner.md)]

Jos sinulla on jo Microsoft Azure Key Vault -viite Regulatory Configuration Service (RCS) -palvelussa, voit luoda viittaukset Key Vaultin varmenteisiin ja salaisiin koodeihin. Jos sinulla ei vielä ole Key Vault -viittausta, katso kohdasta [Palveluympäristöt](e-invoicing-service-environments.md) lisätietoja sen luomista varten.

## <a name="create-certificates-and-secrets"></a>Luo varmenteet ja salaiset koodit

Näiden ohjeiden avulla voit luoda ja määrittää varmenteet ja salaiset koodit.

1. Kirjaudu RCS-tilille.
2. Valitse **Globalisaatio-ominaisuudet**-työtilan **Ympäristö**-osassa **Sähköinen laskutus** -ruutu.
3. Valitse **Ympäristön määritys** -sivun toimintoruudusta **Palveluympäristöt**.
4. Valitse **Palveluympäristöt**-sivun toimintoruudusta **Key Vault -parametrit**.
5. Valitse **Key Vault -parametrit** -sivulla Key Vault -viite ja sitten **Varmenteet**-osasta **Lisää**.
6. Syötä **Nimi**-kenttään avainsäilön varmenteen tai salaisen koodin nimi. Lisätietoja: [Azure-tallennustilin luominen Azure-portaalissa](e-invoicing-create-azure-storage-account-azure-portal.md).
7. Syötä **Kuvaus**-kenttään kuvaus.
8. Valitse **Tyyppi**-kentästä **Varmenne**, jos viittaat varmenteeseen, joka on tallennettu Key Vaultiin. Valitse **Salainen koodi**, jos viittaat näppäimeen salaiseen koodiin, joka on tallennettu Key Vaultiin.
9. Valitse **Tallenna**.

> [!NOTE]
> Joissakin tilanteissa on käytettävä julkisia varmenteita, joilla on tiedostonimen tunniste .cer. Key Vault ei kuitenkaan tue tämän tyypin sertifikaattien tuomista ja tallentamista Key Vault -varmenteiksi. Näissä tilanteissa .cer-tiedosto on tallennettava Base-64-koodattuna X.509 (.CER) -merkkijonona. Tallenna sitten Key Vault -salaisuudessa merkkijono **BEGIN CERTIFICATE** -rivin ja **END CERTIFICATE** -rivin välillä. Palveluympäristössä on edelleen luotava viite Key Vault -tietueeseen ja määritettävä **Tyyppi**-kentän arvoksi **Varmenne**.

## <a name="create-a-chain-of-certificates"></a>Varmenneketjun luominen

Jos maa- tai aluekohtaiset laskut edellyttävät sertifikaattiketjua digitaalisten allekirjoitusten kohdistamiseksi tai suojatun Secure Sockets Layer (\[SSL\]) -yhteyden muodostamiseksi ulkoisiin Internet-palveluihin, luo sertifikaattiketju, jossa sertifikaatit ovat seuraavassa järjestyksessä:

1. Juurivarmenteet
2. Välivarmenteet
3. Loppukäyttäjien varmenteet

Juurivarmenneviranomaiset (CA) ovat sertifikaattien luotettava lähde. CA-välisertifikaatit ovat välisertifikaatteja, jotka linkittävät loppukäyttäjän sertifikaatit CA-juurisertifikaatteihin.

Voit luoda ja määrittää varmenneketjun noudattamalla seuraavia ohjeita.

1. Valitse **Key Vault -parametrit** -sivun toimintoruudusta **Varmenneketju**.
2. Valitse **Uusi**, jos haluat luoda varmenneketjun.
3. Syötä **Nimi**-kenttään varmenneketjun nimi.
4. Syötä **Kuvaus**-kenttään kuvaus.
5. Lisää ketjuun varmenne valitsemalla **Varmenteet**-osasta **Lisää**.
6. Voit muuttaa todistuksen sijaintia ketjussa **Ylös**- tai **Alas**-painikkeella. Säilytä CA-juurisertifikaatti luettelon yläosassa ja loppukäyttäjän sertifikaatti alaosassa.
7. Valitse **Tallenna**.

Voit luoda tarvittavan määrän Key Vault -viitteitä RCS:ssä. Muista, että tallennustilan jaetun oikeuden allekirjoituksen (SAS) tunnuksen avulla linkitetään tietty palveluympäristö Key Vault -viitteeseen. Voit viitata Key Vaultin varmenteisiin ja salaisiin koodeihin, jotka on tallennettu avainsäilöön ja jotka sisältävät salaisuuden tallennustilan SAS-koodille, jota käytät palveluympäristöä määritettäessä.
