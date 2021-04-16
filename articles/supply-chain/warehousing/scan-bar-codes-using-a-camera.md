---
title: สแกนบาร์โค้ดโดยใช้กล้องในแอปการจัดการคลังสินค้าบนมือถือ
description: หัวข้อนี้จะอธิบายวิธีตั้งค่าแอปการจัดการคลังสินค้าบนมือถือเพื่อที่จะสแกนบาร์โค้ด โดยใช้กล้องบนอุปกรณ์เคลื่อนที่
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831229"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="65002-103">สแกนบาร์โค้ดโดยใช้กล้องในแอปการจัดการคลังสินค้าบนมือถือ</span><span class="sxs-lookup"><span data-stu-id="65002-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65002-104">หัวข้อนี้จะอธิบายวิธีตั้งค่าแอปการจัดการคลังสินค้าบนมือถือเพื่อที่จะสแกนบาร์โค้ด โดยใช้กล้องบนอุปกรณ์เคลื่อนที่</span><span class="sxs-lookup"><span data-stu-id="65002-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="65002-105">ตั้งค่า</span><span class="sxs-lookup"><span data-stu-id="65002-105">Setup</span></span>

<span data-ttu-id="65002-106">ในการตั้งค่าการแสดงของแอปการจัดการคลังสินค้าบนมือถือ คุณสามารถเลือกได้ว่า กล้องควรจะใช้สำหรับการสแกนบาร์โค้ดหรือไม่</span><span class="sxs-lookup"><span data-stu-id="65002-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="65002-107">ถ้าคุณเปิดใช้งาน **ใช้กล้องเป็นสแกนเนอร์** คุณสามารถใช้กล้องในทุกฟิลด์อินพุทที่มีโหมดอินพุทที่ต้องการ ซึ่งตั้งค่าเป็น **การสแกน** ได้</span><span class="sxs-lookup"><span data-stu-id="65002-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="65002-108">เพื่อควบคุมว่าฟิลด์ป้อนข้อมูลควรสามารถสแกนได้หรือไม่ ในหน้า **ชื่อฟิลด์แอพ Warehouse** ให้ตั้งค่า **วิธีการป้อนข้อมูลที่ต้องการ** เป็น **การสแกน**.</span><span class="sxs-lookup"><span data-stu-id="65002-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="65002-109">เมื่อมีการเลือกตัวเลือกนี้ คุณสามารถใช้กล้องสำหรับการสแกนในแอปการจัดการคลังสินค้าบนมือถือได้</span><span class="sxs-lookup"><span data-stu-id="65002-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="65002-110">สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [ตั้งค่าฟิลด์สำหรับแอปการจัดการคลังสินค้าบนมือถือ](configure-app-field-names-priorities-warehouse.md)</span><span class="sxs-lookup"><span data-stu-id="65002-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="65002-111">รูปแบบบาร์โค้ดที่สนับสนุน</span><span class="sxs-lookup"><span data-stu-id="65002-111">Supported bar code formats</span></span>

<span data-ttu-id="65002-112">รูปบาร์โค้ดทั่วไปส่วนใหญ่ได้รับการสนับสนุน ซึ่งรวมถึงรหัส 128 รหัส 39 รหัส 93 EAN-8 EAN-13 UPC-E UPC-A และรหัส QR</span><span class="sxs-lookup"><span data-stu-id="65002-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="65002-113">การนำทาง</span><span class="sxs-lookup"><span data-stu-id="65002-113">Navigation</span></span>

<span data-ttu-id="65002-114">หน้ากล้องจะถูกเริ่มในแต่ละหน้าที่ฟิลด์อินพุทมี **โหมดอินพุทที่ต้องการ** ซึ่งถูกตั้งค่าเป็น *การสแกน* เมื่อคุณอยู่ที่หน้ากล้อง ให้ใช้ตัวเลือกต่อไปนี้เพื่อนำทาง:</span><span class="sxs-lookup"><span data-stu-id="65002-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="65002-115">เลือกปุ่มย้อนกลับเพื่อย้อนกลับไปยังหน้า **งานและรายละเอียด**</span><span class="sxs-lookup"><span data-stu-id="65002-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="65002-116">เลือกดินสอบนหน้า **งานและรายละเอียด** เพื่อไปยังหน้าซึ่งคุณสามารถพิมพ์อินพุทได้ด้วยตนเอง</span><span class="sxs-lookup"><span data-stu-id="65002-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="65002-117">เลือกกล้องบนหน้า **งานและรายละเอียด** เพื่อย้อนกลับไปยังหน้ากล้อง</span><span class="sxs-lookup"><span data-stu-id="65002-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="65002-118">บนหน้ากล้อง เมื่อคุณเลือกปุ่มกล้อง จะปรากฏเป็นจางลง ขณะที่พยายามระบุบาร์โค้ด</span><span class="sxs-lookup"><span data-stu-id="65002-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="65002-119">ถ้าไม่มีการระบุบาร์โค้ดภายใน 5 วินาที กระบวนการจะหมดเวลา และปุ่มกล้องจะกลายเป็นพร้อมใช้งานอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="65002-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="65002-120">จากนั้น คุณจะสามารถลองสแกนบาร์โค้ดได้อีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="65002-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="65002-121">เมื่อคุณหันกล้องไปที่บาร์โค้ด รักษาให้บาร์โค้ดอยู่ในระดับภายในเครื่องหมายวงเล็บเพื่อผลลัพธ์ที่ดีที่สุด</span><span class="sxs-lookup"><span data-stu-id="65002-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="65002-122">เมื่อมีการสแกนบาร์โค้ดเสร็จเรียบร้อยแล้ว ผลลัพธ์จะถูกประมวลผล และคุณจะถูกนำไปยังขั้นตอนถัดไป</span><span class="sxs-lookup"><span data-stu-id="65002-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="65002-123">ถ้าขั้นตอนถัดไปประกอบด้วย ฟิลด์อินพุทอีกฟิลด์หนึ่งที่มีโหมดอินพุทที่ต้องการซึ่งถูกตั้งค่าเป็น การสแกน หน้ากล้องจะเริ่มต้นอีกครั้ง</span><span class="sxs-lookup"><span data-stu-id="65002-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="65002-124">ถ้าขั้นตอนถัดไปไม่ใช่ฟิลด์การสแกน จากนั้นหน้ากล้องจะไม่มีการเริ่มต้น</span><span class="sxs-lookup"><span data-stu-id="65002-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]