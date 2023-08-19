
# TypeScript-AppWrite-API-Layer
This is a custom TypeScript layer to use AppWrite database.

An example:

    const { createItem, 
            getItem,
            updateItem,
            deleteItem,
            countItems,
            getList,
            getAllItems } = useCardResource()

> Create Item 

    const item = await createItem(deckModel) // (input: IBaseModel, output: BaseType)

> Get Item
  
      const item = await getItem("mr1n219cb1x2y1kfh")


> Update Item 

    const item = await updateItem(deckModel) // (input: BaseType, output: BaseType)


> Delete Item 

    const item = await deleteItem("nl2e1bjke21bie12zbda") // (input: BaseType, output: BaseType)
> Count Items

    const count = await countItems([ResourceQuery.greaterThan('age', 21)])

> Get List (paginated data)

     const items = await getList(1, 100)


> Get All Items (recursively collect data used getList)

     const items = await getAllItems([ResourceQuery.orderDesc('id'), ResourceQuery.limit(10)])





