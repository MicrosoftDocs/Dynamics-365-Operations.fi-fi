---
title: Kassamoduulin virheiden viitekoodit
description: Tässä artikkelissa kerrotaan kassamoduulin virheiden viitekoodit, jotka näkyvät Microsoft Dynamics 365 Commercen käyttäjille näytettävissä virhesanomissa.
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728242"
---
# <a name="checkout-module-error-reference-codes"></a>Kassamoduulin virheiden viitekoodit

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä artikkelissa kerrotaan kassamoduulin virheiden koodit, jotka näkyvät Microsoft Dynamics 365 Commercen käyttäjille näytettävissä virhesanomissa.

Dynamics 365 Commercessa on otettu käyttöön standardoidut viitekoodit, jotka voidaan sisällyttää online-asiakkaille näytettäviin online-kanavan kassavirheisiin. Commercen versiossa 10.0.31 ja uudemmissa versioissa kassamoduulin virhesanomat sisältävät virhekoodit. Ne eivät välttämättä näytä tietoja online-asiakkaalle. Virhekoodit viittaavat virheisiin, jotka on kuvattu tässä artikkelissa.

Tämän artikkelin taulukko sisältää löydetystä virheestä riippuen seuraava tiedot:

- Virheen aiheuttaneen ehdon kuvaus tai lisätietoja
- Ympäristön tai maksuyhdistinmääritysten huomioon otettavia tietoja
- Tiedot, joihin voidaan viitata tukipalvelupyynnössä, jos tarvitaan lisätukea

## <a name="prerequisites"></a>Edellytykset

Jos haluat ottaa käyttöön alla olevassa luettelossa kuvatut kassamoduulin virheiden viitekoodit, avaa sivustosi luontityökalusta **Sivuston asetukset \> Laajennus** ja valitse **Ostoskori ja kassa** -osiosta **Ota käyttöön parannetut verkkokanavan virheiden näyttämisen viestit**. 

## <a name="checkout-module-error-reference-codes"></a>Kassamoduulin virheiden viitekoodit

Seuraavan taulukon avulla saat lisätietoja virhekoodien viitteistä, jotka asiakkaat antavat tai jotka saadaan verkkokaupasta. Vieritä näyttöä oikealle nähdäksesi **Virheen kuvaus** -sarakkeen.

| Virhekoodi | Dynamicsiin liittyvä virhekoodi | Virheen kuvaus |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | Maksua ei voitu valtuuttaa. **TokenizedPaymentCard**-kohdan korttityypin tunnus puuttuu tai annettua korttityypin tunnusta ei tueta. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Hylätty. Maksua ei voitu valtuuttaa. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | Maksua ei voitu valtuuttaa. Asiakkaan on annettava lisätietoja. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | Tapahtui virhe. Korttimaksun hyväksyntätulosta ei voi noutaa. Yritä uudelleen tai ota yhteyttä järjestelmänvalvojaan. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Maksua ei voi tehdä puuttuvien kauppiaan maksun ominaisuuksien vuoksi. Ota yhteyttä järjestelmänvalvojaan. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | Toiminnon maksuvälinepalvelua ei voi noutaa. Tarkista valitun maksuvälinetyypin maksutavan asetukset. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | Asiakastilin maksu on jo otettu käyttöön. Vain yksi maksu sallitaan transaktiota kohti. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | Asiakastilin raja-arvo on eri kuin erääntyvä summa. Yritä käyttää toista maksutapaa tai ota yhteyttä asiakastukeen. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | Asiakastilin maksu ylittää luettelossa olevien nimikkeiden erääntyvän kokonaissumman. Yritä myöhemmin uudelleen tai ota yhteyttä asiakastukeen. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Asiakastilin maksu vaatii oman tilinsä tai vastaavan laskutustilin maksuvälinerivillä. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Asiakastilin maksua ei voida käsitellä tällä hetkellä – raja-arvo ylitetty. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Tämä asiakas ei voi maksaa tilille. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | Tapahtui virhe. Maksua ei voitu peruuttaa. Yritä uudelleen. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | Virhe maksun käsittelyssä. Yritä myöhemmin uudelleen. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Kanta-asiakasmaksun summa on suurempi kuin mitä tässä tapahtumassa käytetylle kanta-asiakaskortille sallitaan. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Kanta-asiakashyvityksen summa on suurempi kuin mitä tässä tapahtumassa käytetylle kanta-asiakaskortille sallitaan. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Kanta-asiakaskortin numeroa ei löytynyt. Aktivoi kanta-asiakaskortin numero tai syötä toinen kortin numero. Yritä uudelleen. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Kanta-asiakaskortti numero ei ole käytettävissä. Syötä toinen kortin numero ja yritä uudelleen. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Tällä kanta-asiakaskortilla ei voi lunastaa kanta-asiakkuuspisteitä tässä tapahtumassa. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | Virhe lahjakortin numerossa. Yritä käyttää toista lahjakorttia tai ota yhteyttä asiakastukeen. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Summa ylittää lahjakortin jäljellä olevan summan. Syötä toinen summa ja yritä uudelleen. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | Tapahtuma ei voi sisältää enempää kuin yhden kanta-asiakasmaksurivin. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | Maksutiedot puuttuvat tai ne ovat virheellisiä. Tarkista maksutiedot ja yritä uudelleen. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | Tilausta ei voi käsitellä nyt. Yritä myöhemmin uudelleen. |
| CCR025     | Kassan ohjelmointirajapinnan edustan aikakatkaisu | Taustatoiminto aikakatkaistiin. Tarkista, onko tilaus käsitelty Dynamics 365 Commerce headquartersissa. |
| CCR026     | Alkuperäistä valtuutettua summaa on muutettu | Tilauksen summaa on muutettu maksuyhdyskäytävässä käsitellystä alkuperäisestä valtuutussummasta. Tämä voi johtua kupongin, kampanjan tai myynnin ajoitetusta vanhenemisesta. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | Virhe maksun käsittelyssä. Ostoskorin ohjelmointirajapinnalle määritetty viite on eri kuin odotettu viite (osoittaa mahdollisen ristiriidan kassaprosessin aikana). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | Maksutapa, jota yritettiin käyttää, päättyi virheeseen. Ota yhteyttä tukeen, jos haluat tarkistaa tilin asetukset, tai yritä uudelleen eri maksutavalla. |

## <a name="additional-resources"></a>Lisäresurssit

[Maksut – usein kysytyt kysymykset](dev-itpro/payments-retail.md)

[Kassamoduuli](add-checkout-module.md)

[Maksumoduuli](payment-module.md)
