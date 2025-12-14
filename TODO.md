# TODO: Add Add/Reduce Stock Functions and Logs Section

## Step 1: Add Add/Reduce Stock Buttons and Modal
- Add "Add Stock" and "Reduce Stock" buttons to the inventory table actions.
- Create a new modal for inputting quantity to add or reduce.
- Add CSS for the new modal.

## Step 2: Implement Add/Reduce Stock JavaScript Functions
- Create functions `showAddStockModal(id)`, `showReduceStockModal(id)`, `addStock(id, quantity)`, `reduceStock(id, quantity)`.
- Validate that reducing doesn't go below 0.
- Update inventory in Firestore (online) or localStorage (offline), save pending changes.
- Refresh inventory table and check low stock after update.

## Step 3: Add Logs Tab and Data Structure
- Add a new "Logs" tab button in the tabs section.
- Add a new tab-content div for logs.
- Initialize a logs array and sync with Firebase collection 'logs' or localStorage.
- Create log entry structure: { type, details, timestamp }

## Step 4: Implement Logging for All Activities
- Log sales when added: type 'sale', details include sale data.
- Log inventory stock changes: type 'stock_add' or 'stock_reduce', details include item name, quantity changed, new total.
- Log item operations: 'item_add', 'item_edit', 'item_delete', details include item data.
- Add logging calls in respective functions (addSale, saveItem, deleteItem, addStock, reduceStock).

## Step 5: Display Logs in Table
- Create renderLogsTable function to display logs sorted by timestamp descending.
- Show columns: Date/Time, Type, Details.
- Load logs on app load and refresh after changes.

## Step 6: Test and Finalize
- Test add/reduce stock in online and offline modes.
- Test logging for all activities.
- Ensure low stock checks trigger after stock changes.
- Verify logs display correctly.
