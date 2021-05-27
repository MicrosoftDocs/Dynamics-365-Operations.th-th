---
title: ตั้งค่ารหัสภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS
description: หัวข้อนี้อธิบายวิธีการตั้งค่ารหัสภาษีสำหรับภาษีที่หักที่ต้นทาง (TDS)
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023640"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="3ddf5-103">ตั้งค่ารหัสภาษีหัก ณ ที่จ่ายสำหรับชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ddf5-104">หัวข้อนี้อธิบายวิธีการตั้งค่ารหัสภาษีสำหรับภาษีที่หักที่ต้นทาง (TDS)</span><span class="sxs-lookup"><span data-stu-id="3ddf5-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="3ddf5-105">ไปที่ **ภาษี \> ภาษีทางอ้อม \> ภาษีหัก ณ ที่จ่าย \> รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="3ddf5-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="3ddf5-106">[![หน้ารหัสภาษีหัก ณ ที่จ่าย](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="3ddf5-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="3ddf5-107">ในบานหน้าต่างการดำเนินการ เลือก **ใหม่** เพื่อสร้างรหัสภาษีหัก ณ ที่จ่ายสำหรับ TDS และป้อนรายละเอียดที่จำเป็น</span><span class="sxs-lookup"><span data-stu-id="3ddf5-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="3ddf5-108">บน FastTab **ทั่วไป** ในฟิลด์ **ชนิดภาษี** ให้เลือก **TDS** เพื่อจัดประเภทรหัสภาษีเป็นรหัสภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="3ddf5-109">ในฟิลด์ **รอบระยะเวลาการชําระเงิน** ให้เลือกรอบระยะเวลาการชําระเงิน TDS สำหรับรหัสภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="3ddf5-110">ในฟิลด์ **บัญชีหลัก** เลือกบัญชีแยกประเภทที่ยอดเงิน TDS ควรจะได้รับการลงรายการบัญชี</span><span class="sxs-lookup"><span data-stu-id="3ddf5-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="3ddf5-111">ในฟิลด์ **บัญชีลูกหนี้** ให้เลือกบัญชีลูกหนี้ที่ควรมีการลงรายการบัญชียอดเงิน TDS ที่ถูกหักในธุรกรรมการขาย</span><span class="sxs-lookup"><span data-stu-id="3ddf5-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="3ddf5-112">ฟิลด์ **จุดเริ่มต้น** มีการตั้งค่าเป็น **เปอร์เซ็นต์ของยอดเงินรวม** โดยอัตโนมัติ และไม่สามารถเปลี่ยนค่าได้</span><span class="sxs-lookup"><span data-stu-id="3ddf5-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ddf5-113">คุณไม่สามารถตั้งค่าจุดเริ่มต้นเป็น **เปอร์เซ็นต์ของยอดเงินสุทธิ** สำหรับรหัสภาษีของชนิดภาษี TDS ได้</span><span class="sxs-lookup"><span data-stu-id="3ddf5-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="3ddf5-114">ในฟิลด์ **ส่วนประกอบภาษีหัก ณ ที่จ่าย** เลือกส่วนประกอบภาษี TDS สำหรับรหัสภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="3ddf5-115">ในบานหน้าต่างการดำเนินการ เลือก **ค่า** เพื่อเปิดหน้า **ค่าภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="3ddf5-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="3ddf5-116">ในฟิลด์ **วันที่เริ่มต้น** ป้อนวันที่เริ่มต้นสำหรับค่า TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="3ddf5-117">ในฟิลด์ **วันที่สิ้นสุด** ให้ป้อนวันที่สิ้นสุด</span><span class="sxs-lookup"><span data-stu-id="3ddf5-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ddf5-118">ฟิลด์ **ขีดจํากัดต่ำสุด**, **ขีดจํากัดสูงสุด** และ **ไม่รวม %** ไม่พร้อมใช้งานสำหรับรหัสภาษีของชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="3ddf5-119">ในฟิลด์ **ค่า** ป้อนเปอร์เซ็นต์ของ TDS สำหรับรหัสภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="3ddf5-120">ปิดหน้า **ค่าภาษีหัก ณ ที่จ่าย** เพื่อกลับไปที่หน้า **รหัสภาษีหัก ณ ที่จ่าย**</span><span class="sxs-lookup"><span data-stu-id="3ddf5-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ddf5-121">ปุ่ม **ขีดจํากัด** บนหน้ารหัส **ภาษีหัก ณ ที่จ่าย** ไม่พร้อมใช้งานสำหรับรหัสภาษีของชนิดภาษี TDS</span><span class="sxs-lookup"><span data-stu-id="3ddf5-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="3ddf5-122">ปิดหน้า</span><span class="sxs-lookup"><span data-stu-id="3ddf5-122">Close the page.</span></span>
