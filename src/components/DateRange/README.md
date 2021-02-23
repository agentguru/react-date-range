This component extends all the props of **[Calendar](#calendar)** component. In addition to those props, it has the following props: 

| Prop Name  |  Type |
|---|---|
|  **moveRangeOnFirstSelection** |  boolean |
|   **onRangeFocusChange** |  function |
|   **rangeColors**  |  array |
|   **ranges**  |  array |


#### Example: Editable Date Inputs
```jsx inside Markdown
import {useState} from 'react'
const [state, setState] = useState([
    {
      startDate: null,
      endDate: null,
      key: 'selection'
    }
  ]);
  
<DateRange
  editableDateInputs={true}
  onChange={item => setState([item.selection])}
  moveRangeOnFirstSelection={false}
  ranges={state}
  className="calendar"
  months={3}
  minDate={new Date()}
  dragSelectionEnabled
  direction="vertical"
  scroll={{ enabled: true, monthHeight: 320 }}
  showDateDisplay={false}
  showMonthAndYearPickers={false}
/>
```
