and s.FOLLOWING_ID not in (select nvl(t.FOLLOWING_ID,-1) from tbl_transport t where t.CANCEL_DATE is null and t.shipment_type_id in (0,1,17,18,22,23,24))

                               and ( s.MILKRUNID is null or s.IS_MAIN_MILK = 1)  

                                and s.FOLLOWING_ID not in (select nvl(tt.FOLLOWING_ID,-1) from TBL_TRANSPORT_DETAIL tt   where tt.expire_date  is null)

                                and ( s.PACK_GROUP_ID = 1 or s.DEST_LOADINGSTATION_ID = s.PALET_LOADING_ID)

                                and s.REJECT_ِDATE is null 

                                and s.WAY_BILL_receipt_id is null


and s.FOLLOWING_ID not in (select nvl(t.FOLLOWING_ID,-1) from tbl_transport t where t.CANCEL_DATE is null and t.shipment_type_id in (17,18,22,23,24))

                               and ( s.MILKRUNID is null or s.IS_MAIN_MILK = 1)  

                                and s.FOLLOWING_ID not in (select nvl(tt.FOLLOWING_ID,-1) from TBL_TRANSPORT_DETAIL tt   where tt.expire_date  is null)

                                and ( s.PACK_GROUP_ID = 1 or s.DEST_LOADINGSTATION_ID = s.PALET_LOADING_ID)

                                and s.REJECT_ِDATE is null 

                                and s.WAY_BILL_receipt_id is null



با سلام و احترام

درخصوص گفتگوهاي انجام شده توضيحات زير خدمتتان ارائه ميگردد:

فرم ثبت اطلاعات حمل هاي آيكيد براساس منطق زير عمل ميكند:

با ويو دريافتي از سمت ايسيكو براساس كدرهگيري و فيلدهاي ارسالي در اسكرين شات اطلاعات از ويو خوانده شده و نمايش داده ميشود.

براي نمايش در ابتدا از فيلتري براساس تاريخ (از تاريخ تا تاريخ) جستجو انجام ميشود.

پس از نمايش با امكان سرچ كردن كدهاي رهگيري و سپس انتخاب حمل با كليك بر روي دكمه "تاييديه حمل اصلي" امكان تغيير برخي از فيلدهاي ديتا و انتخاب راننده و .... و ثبت حمل اطلاعات حمل در TBL_TRANSPORT ثبت و ذخيره ميگردد.

نمونه ارسالي فايل اكسل به منظور فيلدها در زمان نمايش اطلاعات حمل ها در صفحه اصلي مي باشد.

لازم به ذكر است نيازمند امكان گرفتن خروجي از ليست نمايش حمل ها نيز مي باشيم.

با سپاس

...