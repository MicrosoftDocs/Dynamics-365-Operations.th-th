---
title: การสนับสนุนบาร์โค้ดบนมือถือ
description: หัวข้อนี้อธิบายวิธีการจัดการแอพสแกนอุปกรณ์เคลื่อนที่ของคลังสินค้าบนอุปกรณ์ที่เข้ากันได้กับ Android
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462d35ebf1015ace032c523a4efe92bc7594ba3c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 09/24/2019
ms.locfileid: "2027011"
---
# <a name="mobile-bar-code-support"></a><span data-ttu-id="6db6a-103">การสนับสนุนบาร์โค้ดบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="6db6a-103">Mobile bar code support</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6db6a-104">เนื่องจาก Android คือ โครงการที่มีแหล่งที่มาแบบเปิด ผู้ผลิตฮาร์ดแวร์ใดๆ สำหรับเครื่องสแกนบาร์โค้ดของคลังสินค้า สามารถสร้างอุปกรณ์ให้รันระบบปฏิบัติการ Android ได้</span><span class="sxs-lookup"><span data-stu-id="6db6a-104">Because Android is an open source project, any manufacturer of hardware for warehouse bar code scanners can build a device to run the Android operating system.</span></span> <span data-ttu-id="6db6a-105">อุปกรณ์จะเข้ากันได้กับ Android เท่านั้น ถ้าสามารถรันแอพที่ถูกเขียนขึ้นสำหรับสภาพแวดล้อมการดำเนินการ Android</span><span class="sxs-lookup"><span data-stu-id="6db6a-105">A device is only Android-compatible if it can run apps that are written for the Android execution environment.</span></span>
<span data-ttu-id="6db6a-106">อย่างไรก็ตาม ผู้จัดจำหน่ายฮาร์ดแวร์สามารถแก้ไขและสร้างการซ้อนทับ สำหรับรุ่น Android ที่รันบนฮาร์ดแวร์</span><span class="sxs-lookup"><span data-stu-id="6db6a-106">However, a hardware vendor can modify and create overlays for the Android version that runs on their hardware.</span></span> <span data-ttu-id="6db6a-107">Microsoft ไม่สามารถแสดงความรับผิดชอบใดๆ เพื่อให้แน่ใจว่าแอพสแกนบาร์โค้ดของอุปกรณ์เคลื่อนที่สำหรับ Android เข้ากันได้กับฮาร์ดแวร์เครื่องสแกนบาร์โค้ดของผู้ผลิตและรุ่น Android ที่รันบนนั้น</span><span class="sxs-lookup"><span data-stu-id="6db6a-107">Microsoft cannot take any responsibility to ensure that a mobile bar code scanning app for Android is compatible with a manufacturer’s bar code scanning hardware and the Android version that runs on it.</span></span> 

<span data-ttu-id="6db6a-108">The Dynamics 365 Supply Chain Management แอพลิเคชัน Warehousing ได้รับการทดสอบด้วยตัวเลือกอุปกรณ์ที่ทำงานบน Android สำหรับการสแกนบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="6db6a-108">The Dynamics 365 Supply Chain Management - Warehousing app has been tested with a selection of Android powered devices for bar code scanning.</span></span> <span data-ttu-id="6db6a-109">การทดสอบเหล่านี้ครอบคลุมตัวอย่างของอุปกรณ์ที่มีอยู่ในตลาดเท่านั้น</span><span class="sxs-lookup"><span data-stu-id="6db6a-109">These tests only cover a sample of the devices that are available on the market.</span></span>

<span data-ttu-id="6db6a-110">ในฐานะลูกค้า เราขอแนะนำให้คุณทดสอบที่แอพสแกนอุปกรณ์เคลื่อนที่ของคลังสินค้าบนฮาร์ดแวร์ที่เลือก ก่อนที่คุณจะตัดสินใจเกี่ยวกับฮาร์ดแวร์ที่คุณต้องการซื้อ</span><span class="sxs-lookup"><span data-stu-id="6db6a-110">As a customer, we recommend that you test the Warehouse mobile scanning app on selected hardware before you decide on the hardware that you want to buy.</span></span>

