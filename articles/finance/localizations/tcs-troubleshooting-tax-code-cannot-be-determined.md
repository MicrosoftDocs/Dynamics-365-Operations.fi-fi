---
title: Verokoodia ei voi määrittää
description: Tässä aiheessa kerrotaan, miten verolaskentapalvelun "Verokoodia ei voi määrittää" -virhettä korjataan.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645389"
---
# <a name="tax-code-cannot-be-determined"></a>Verokoodia ei voi määrittää

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten tehdään vianetsintää, kun verolaskentapalvelun "Verokoodia ei voi määrittää" -virhettä korjataan.

## <a name="symptom"></a>Oire

Näkyviin tulee seuraava virhesanoma: ”Otsikko/Rivit - 1, verokoodia ei voi määrittää”. Voit myös löytää virheen vianmääritystiedostossa seuraavan esimerkin mukaisesti. Lisätietoja on kohdassa [Virheenkorjaustilan ottaminen käyttöön vianetsintään](tcs-troubleshooting-enable-debug-mode.md).

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Syy

Ongelma esiintyy todennäköisesti, koska veroryhmä ja nimikkeen veroryhmä eivät leikkaa.

## <a name="troubleshoot"></a>Vianmääritys

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Varmista vianmääritystiedostossa, että veroryhmä ja nimikkeen veroryhmä on määritetty. Jos **veroryhmän** ja **nimikkeen veroryhmän** arvot ovat tyhjiä, veroryhmää ja nimikkeen veroryhmää ei ole määritetty. Jos ne on määritetty, tulokset saattavat olla virheellisiä.

    Esimerkki vianmääritystiedostosta.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
                            "Adjustment": null
                        }
                    ],
                    "Measures": {
                        ...
                    },
                    ...
                }
            ]
        },
        ...
    }
    ```

2. Varmista, että myyntitilausrivin tietojen **Asetukset**-välilehden **Ohita arvonlisävero** -asetus on käytössä.

    - Jos se on käytössä, verokoodit määräytyvät tapahtumariville syöttämiesi **Veroryhmä**- ja **Nimikkeen veroryhmän** -arvojen mukaan. Tarkista, että nämä arvot on syötetty oikein.
    - Jos sitä ei ole otettu käyttöön, varmista , että **Veroryhmän käytettävyys**- ja **Nimikeveroryhmän käytettävyys** -kentille on määritetty oikeat arvot. Lisätietoja on kohdassa [Vastaavia tuloksia ei löydy](tcs-troubleshooting-no-matching-result.md).

3. Jos veroryhmä ja nimikkeen veroryhmä on määritetty oikein, määritä, onko niillä yhteisiä arvoja.

    1. Siirry RCS:ssä kohtaan **Vero-ominaisuudet** \> **Verokoodit ja -ryhmät** \> **Veroryhmä**.

        | Line.Tax -ryhmä | Verokoodit |
        |----------------|-----------|
        | Ryhmä A        | A         |

    2. Siirry kohtaan **Vero-ominaisuudet** \> **Verokoodit ja -ryhmät** \> **Nimikkeen veroryhmä**.

        | Line.Item -veroryhmä | Verokoodit |
        |---------------------|-----------|
        | Ryhmä B             | D         |

    Jos veroryhmällä ja nimikkeen veroryhmällä ei ole yhteisiä arvoja, verokoodia ei määritetä.

## <a name="mitigation"></a>Lievennys

1. Käy tämän ohjeaiheen [Vianmääritys](#troubleshoot)-osa läpi ja korjaa asetukset tarvittaessa. Jos veroryhmää ja nimikkeen veroryhmää ei ole määritetty oikein, katso lisätietoja kohdasta [Vastaavia tuloksia ei löydy](tcs-troubleshooting-no-matching-result.md).
2. Jos veroryhmällä ja nimikkeen veroryhmällä ei ole yhteisiä arvoja, luo uusi toimintoversio RCS:ssä ja korjaa asetukset.

    - Siirry kohtaan **Vero-ominaisuudet** \> **Verokoodit ja -ryhmät** >  **Nimikkeen veroryhmä**.

        | Line.Item -veroryhmä | Verokoodit |
        |---------------------|-----------|
        | Ryhmä B             | A;B       |

    Verokoodiksi määritetään **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
