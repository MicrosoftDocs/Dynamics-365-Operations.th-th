---
title: ราคาขายสำหรับการบอกรับเป็นสมาชิก
description: เมื่อคุณสร้างการบอกรับเป็นสมาชิก คุณจะได้รับราคาขายจากการตั้งค่าราคาขายซึ่งถูกสร้างในแบบฟอร์มราคาขาย (การบอกรับเป็นสมาชิก)
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ed8329e9da08fbe24d9b3982eee562974f0fb3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: th-TH
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242312"
---
# <a name="subscription-sales-prices"></a>ราคาขายสำหรับการบอกรับเป็นสมาชิก   

[!include [banner](../includes/banner.md)]


เมื่อคุณสร้างการบอกรับเป็นสมาชิก คุณจะได้รับราคาขายจากการตั้งค่าราคาขายซึ่งถูกสร้างในแบบฟอร์ม **ราคาขาย (การบอกรับเป็นสมาชิก)**

ในแบบฟอร์ม **ราคาขาย (การบอกรับเป็นสมาชิก)** คุณสามารถสร้างราคาขายสำหรับการบอกรับสมาชิกที่กำหนดไว้ได้ หรือคุณอาจสร้างราคาขายที่นำไปใช้ได้อย่างกว้างขวางขึ้นได้ สำหรับราคาขายที่จะนำไปใช้ในการบอกรับเป็นสมาชิก รหัสรอบระยะเวลาและสกุลเงินของการบอกรับเป็นสมาชิก ต้องเหมือนกับรหัสรอบระยะเวลาและสกุลเงินของราคาขาย

หากรหัสรอบระยะเวลาและสกุลเงินของทั้งการบอกรับเป็นสมาชิกและราคาขายเหมือนกัน จะมีการเลือกราคาขายสำหรับการบอกรับเป็นสมาชิกตามระดับความสำคัญที่แสดงรายการในตารางต่อไปนี้ เซลล์ว่างในตารางจะหมายถึงฟิลด์ว่าง และ X หมายถึงค่าที่เท่ากับค่าในการบอกรับเป็นสมาชิกจากธุรกรรมที่สร้างขึ้น

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ระดับความสำคัญ </p></th>
<th><p><strong>ประเภท</strong></p></th>
<th><p><strong>รหัสโครงการ</strong></p></th>
<th><p><strong>การสั่งซื้อโดยบอกรับเป็นสมาชิก</strong></p></th>
<th><p><strong>สกุลเงินที่ใช้ในการขาย</strong></p></th>
<th><p><strong>ชนิดรอบระยะเวลาบัญชี</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4 ชั่วโมง</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6 ชั่วโมง</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>


เมื่อมีการสร้างค่าธรรมเนียมการบอกรับเป็นสมาชิก ราคาขายที่มีระดับรายละเอียดมากที่สุด (ตามที่ระบุไว้ในตารางข้างต้น) จะถูกเลือกเป็นราคาขายสำหรับการบอกรับเป็นสมาชิก

## <a name="update-and-index-subscription-sales-prices"></a>การอัพเดตและการจัดดัชนีราคาขายของการสั่งซื้อโดยบอกรับเป็นสมาชิก

คุณสามารถอัพเดตราคาขายสำหรับการสั่งซื้อโดยบอกรับเป็นสมาชิกโดยการอัพเดตราคาหรือดัชนีพื้นฐาน คุณสามารถอัพเดตตามเปอร์เซ็นต์หรือค่าใหม่ได้

## <a name="subscription-fee-sales-prices"></a>ราคาขายสำหรับค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก

เมื่อคุณสร้างค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิก ราคาขายจะขึ้นอยู่กับการตั้งค่าราคาขายของการบอกรับเป็นสมาชิก  คุณสามารถใช้ราคาพื้นฐานจากการตั้งค่าราคาการบอกรับเป็นสมาชิก หรือคุณอาจสร้างราคาขายที่มีการจัดทำดัชนีขึ้นก็ได้ อย่างใดอย่างหนึ่ง

## <a name="example"></a>ตัวอย่าง

คุณต้องการตั้งค่าราคาขายของการสั่งซื้อโดยบอกรับเป็นสมาชิกเป็นจำนวนเงิน  EUR 500 สำหรับโครงการใหม่ ในแบบฟอร์ม **ราคาขาย (การบอกรับเป็นสมาชิก)** คุณสร้างรายการราคาขายการบอกรับเป็นสมาชิกตามที่ระบุไว้ในตารางต่อไปนี้

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ใช้ได้ตั้งแต่</p></th>
<th><p>ประเภท</p></th>
<th><p>Project</p></th>
<th><p>การบอกรับเป็นสมาชิก</p></th>
<th><p>ชนิดรอบระยะเวลาบัญชี</p></th>
<th><p>สกุลเงินที่ใช้ในการขาย</p></th>
<th><p>ราคาขาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>วันที่ 28-08-2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>เดือน</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


โปรดจำไว้ว่าฟิลด์ **ประเภท** และ **การบอกรับเป็นสมาชิก** ว่าง

จากนั้น คุณสร้างการบอกรับเป็นสมาชิกดังนี้

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>การบอกรับเป็นสมาชิกการบริการ</p></th>
<th><p>Project</p></th>
<th><p>ประเภทของการบอกรับเป็นสมาชิก</p></th>
<th><p>ประเภท</p></th>
<th><p>สกุลเงิน</p></th>
<th><p>รหัสรอบระยะเวลา</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat1</p></td>
<td><p>EUR</p></td>
<td><p>รายเดือน</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Sub1</p></td>
<td><p>SubCat2</p></td>
<td><p>EUR</p></td>
<td><p>รายเดือน</p></td>
</tr>
</tbody>
</table>


ตอนนี้คุณสร้างค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิกสำหรับการบอกรับเป็นสมาชิกทั้งสองในประเภทของการบอกรับเป็นสมาชิก Sub1:

1.  คลิก **การจัดการงานบริการ** \> **การตั้งค่า** \> **การบอกรับเป็นสมาชิกการบริการ** \> **กลุ่มการบอกรับเป็นสมาชิก**

2.  ในฟอร์ม **กลุ่มการบอกรับเป็นสมาชิก** คลิก **ฟังก์ชัน** \> **สร้างค่าธรรมเนียมการบอกรับเป็นสมาชิก**

3.  ในแบบฟอร์ม **สร้างค่าธรรมเนียมการบอกรับเป็นสมาชิก** ให้ป้อนข้อมูลที่เหมาะสม สำหรับข้อมูลเพิ่มเติม ให้ดูที่ [สร้างธุรกรรมค่าธรรมเนียมสำหรับการบอกรับเป็นสมาชิก](create-subscription-fee-transactions.md)

ค่าธรรมเนียมการบอกรับเป็นสมาชิกที่มีราคาขาย EUR 500 จะถูกสร้างขึ้นสำหรับการบอกรับเป็นสมาชิกทั้งสองรายการ ดังที่แสดงในตารางต่อไปนี้

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>วันที่โครงการ</p></th>
<th><p>การบอกรับเป็นสมาชิกการบริการ</p></th>
<th><p>Project</p></th>
<th><p>ประเภท</p></th>
<th><p>วันที่เริ่มต้น</p></th>
<th><p>วันที่สิ้นสุด</p></th>
<th><p>สกุลเงินที่ใช้ในการขาย</p></th>
<th><p>ราคาขาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>วันที่ 28-08-2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>วันที่ 01-01-2007</p></td>
<td><p>วันที่ 31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>วันที่ 28-08-2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>วันที่ 01-01-2007</p></td>
<td><p>วันที่ 31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


จากนั้น ดังนั้น คุณสร้างรายการราคาขายใหม่ที่มีราคาขายเป็น EUR 550 สำหรับการรวมของโครงการ 9030 และประเภทค่าธรรมเนียม SubCat1 ตอนนี้ จึงมีรายการราคาขายการบอกรับเป็นสมาชิกสองรายการสำหรับโครงการ 9030 ดังที่แสดงอยู่ในตารางต่อไปนี้

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ใช้ได้ตั้งแต่</p></th>
<th><p>ประเภท</p></th>
<th><p>Project</p></th>
<th><p>การบอกรับเป็นสมาชิก</p></th>
<th><p>ชนิดรอบระยะเวลาบัญชี</p></th>
<th><p>สกุลเงิน</p></th>
<th><p>ราคาขาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>วันที่ 28-08-2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>เดือน</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>วันที่ 28-08-2007</p></td>
<td><p>SubCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>เดือน</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


คุณทำขั้นตอนที่อธิบายไว้ข้างต้นซ้ำเพื่อสร้างค่าธรรมเนียมการสั่งซื้อโดยบอกรับเป็นสมาชิกสำหรับการบอกรับเป็นสมาชิกทั้งสองในประเภทของการบอกรับเป็นสมาชิก Sub1 ธุรกรรมสองรายการจะถูกสร้างขึ้น ตารางต่อไปนี้แสดงธุรกรรมที่ถูกสร้างขึ้นสำหรับการบอกรับเป็นสมาชิกแต่ละรายการ ที่ถูกแนบกับกลุ่มการบอกรับเป็นสมาชิก

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>วันที่โครงการ</p></th>
<th><p>การบอกรับเป็นสมาชิก</p></th>
<th><p>Project</p></th>
<th><p>ประเภท</p></th>
<th><p>วันที่เริ่มต้น</p></th>
<th><p>วันที่สิ้นสุด</p></th>
<th><p>สกุลเงินที่ใช้ในการขาย</p></th>
<th><p>ราคาขาย</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>วันที่ 28-07-2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat1</p></td>
<td><p>วันที่ 01-01-2008</p></td>
<td><p>วันที่ 31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>วันที่ 28-07-2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>SubCat2</p></td>
<td><p>วันที่ 01-01-2008</p></td>
<td><p>วันที่ 31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


ในธุรกรรมแรกของการบอกรับเป็นสมาชิก 00020\_135 ราคาขายจำนวน EUR 550 ได้มาจากราคาขายสำหรับการบอกรับเป็นสมาชิกที่ถูกตั้งค่าสำหรับชุดโครงการและประเภทที่กำหนดไว้ ในธุรกรรมที่สองสำหรับการบอกรับเป็นสมาชิก 00021\_135 มีการใช้ราคาขายจำนวน EUR 500 เป็นราคาขายสำหรับการบอกรับเป็นสมาชิกของโครงการ เนื่องจากไม่มีการตั้งค่าราคาสำหรับชุดโครงการ 9030 และประเภท SubCat2

## <a name="see-also"></a>ดูเพิ่มเติมที่

[การอัพเดตและการจัดดัชนีราคาขายของการสั่งซื้อโดยบอกรับเป็นสมาชิก](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]