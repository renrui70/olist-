**  巴西电商数据分析实战项目**
  背景：这是在 Olist Store 下达的订单的巴西电子商务公共数据集。该数据集包含 2016 年至 2018 年在巴西多个市场下达的 100k 个订单的信息。其功能允许从多个维度查看订单：从订单状态、价格、付款和货运绩效到客户位置、产品属性，最后是客户撰写的评论。我们还发布了一个地理位置数据集，将巴西邮政编码与纬度/液化天然气坐标相关联。

  这是真实的商业数据，已被匿名化，评论文本中对公司和合作伙伴的引用已被《权力的游戏》各大家族的名称所取代。

  数据来源：
https://www.kaggle.com/olistbr/brazilian-ecommerce?select=olist_customers_dataset.csv
包括九张表。
（1）olist_customers_dataset：为客户数据集，包含有关客户及其位置的信息。使用它来识别订单数据集中的唯一客户并查找订单交付位置。每个订单都分配给一个唯一的customer_id。这意味着同一买家将获得不同订单的不同 ID。
（2）olist_geolocation_dataset：为地理位置数据集，包含巴西邮政编码及其纬度/液化天然气坐标信息。使用它来绘制地图并查找卖家和客户之间的距离。
（3）olist_order_items_dataset：为订单项数据集，包含有关每个订单中购买的商品的数据，包括产品价格（price）和运费价格（freight_value），其中shipping_limit_date为卖家给物流合作伙伴设定的发货限制日期。
（4）olist_order_payments_dataset：为支付数据集，包含有关订单付款选项的数据，其中payment_installmentss为客户选择的分期付款数。
（5）olist_order_reviews_dataset：为订购评论数据集，包含有关客户所做评论的数据。客户从 Olist Store 购买产品后，卖家会收到通知以履行该订单。一旦客户收到产品或预计交货日期到期，客户将通过电子邮件收到满意度调查，他可以在其中提供购买体验的说明并写下一些评论。
（6）olist_orders_dataset：为订单数据集，是核心数据集。从每个订单中可以找到所有其他信息。其中order_purchase_timestamp为购买时间戳，order_approved_at为付款批准时间戳，order_delivered_carrier_date为订单过账给物流的时间戳，order_delivered_customer_date为客户实际订单交货时间戳，order_estimated_delivery_date为购买时通知客户的预计交货时间。
（7）olist_products_dataset：为产品数据集，包括有关 Olist 销售的产品的数据。
（8）olist_sellers_dataset：为卖家数据集，包括有关履行在 Olist 下的订单的卖家的数据。使用它来查找卖家位置并确定哪个卖家配送了每件商品。
（9）product_category_name_translation：为类别名称翻译，将 product_category_name 翻译成英文。


项目1：sql+powerbi
项目2：python+sql+tableau

对比powerbi和tableau有感：
同样的数据表在绘图的时候，感觉在tableau中更加方便一些。
1.在更改横纵坐标的时候，tableau会更加方便一些，双击选中即可更改，powerbi则需要在右侧设置视觉对象格式-视觉对象-x轴-标题，一层层打开才能进行更改。
2.不同深浅颜色的更改上，tableau只需要拖拽凸显颜色深浅的字段值到标记-颜色即可，powerbi则需要在右侧设置视觉对象格式-视觉对象-数据标签-值-颜色旁边的fx中设置格式样式为渐变，再选择哪个字段，以及具体的最深的颜色和最浅的颜色。如果采用系统默认的最深、最浅的颜色效果不是很明显，还是需要自行选择颜色的，而tableau则采用系统默认的颜色即可。
3.在图例中，tableau不仅可以修改图例的标题，还可以修改图标的名称（因为有的数据集字段采用的是英文，需要更改成中文），而在powerbi中只能更改图例的标题，暂且没找到哪个选项可以更改图标。
4.在横纵坐标的刻度单位中，tableau的单位是用英文k表示千，w表示万，但在powerbi中只能用中文的千、万。
不过在绘制仪表板的时候，powerbi会方便一些，可以直接将好几张图绘制在一张仪表板中，而tableau需要一个个新建工作表，再将工作表拖拽到仪表板中。
