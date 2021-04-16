---
title: การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e
description: หัวข้อนี้ให้ข้อมูลเกี่ยวกับการเปิดใช้งานและการใช้ใบรับรอง NF-e แบบกำหนดเอง
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813979"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="1441e-103">การตรวจสอบความถูกต้องของใบรับรองแบบกำหนดเอง NF-e</span><span class="sxs-lookup"><span data-stu-id="1441e-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1441e-104">เมื่อคุณเปิดใช้งานคุณลักษณะการตรวจสอบใบรับรองแบบกำหนดเอง NF-E การตรวจสอบความถูกต้องแบบกำหนดเองอนุญาตให้มีการเชื่อมต่อกับบริการเว็บ</span><span class="sxs-lookup"><span data-stu-id="1441e-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="1441e-105">การเชื่อมต่อนี้ต้องใช้เพื่อส่ง NF-E และรับการตรวจสอบจาก SEFAZ</span><span class="sxs-lookup"><span data-stu-id="1441e-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="1441e-106">คุณสมบัติ **จุดประสงค์การรับรองความถูกต้องเซิร์ฟเวอร์** จากการรับรอง V5 ออกโดยหน่วยงานใบรับรองหลักของบราซิล</span><span class="sxs-lookup"><span data-stu-id="1441e-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="1441e-107">คุณสมบัตินี้ปิดใช้งานโดยค่าเริ่มต้น และต้องเปิดใช้งานด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="1441e-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="1441e-108">ในบางกรณี การอัปเดตใบรับรองอัตโนมัติสามารถสลับคุณสมบัตินี้เป็นไม่มีการเปิดใช้งานอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="1441e-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="1441e-109">ถ้าเหตุการณ์นี้เกิดขึ้น การเชื่อมต่อ TLS จะได้รับผลกระทบ และไม่ได้รับความไว้วางใจอีกต่อไป</span><span class="sxs-lookup"><span data-stu-id="1441e-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="1441e-110">ความสามารถในการออก NF-E ในสภาพแวดล้อมการผลิตสำหรับรัฐของ Minas Gerais (MG) และ Paraná (PR) มีผลกระทบ</span><span class="sxs-lookup"><span data-stu-id="1441e-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="1441e-111">การอัปเดตนี้ช่วยให้มีโซลูชันอีกวิธีหนึ่งสำหรับการตรวจสอบความถูกต้องของใบรับรอง ซึ่งหมายความว่าคุณสามารถสร้างการสื่อสารที่มีความปลอดภัยได้</span><span class="sxs-lookup"><span data-stu-id="1441e-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]