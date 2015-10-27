import android.app.Activity;
import android.content.DialogInterface;
import android.widget.AdapterView;

/**
 * Created by Safer on 10/20/2015.
 * Tested on Android 4.4 KitKat JVM.
 *
 * Calendar App Change Log:
 * v1.0 - Added Basic UI Interface Support
 *      - User Views: Monthly View (default)
 *      -
 */

public class CalendarView extends Activity {

    public Calendar month;      // Calendar instance
    public Calendar itemonth;   // Calendar instance

    public CalendarAdapter adapter;     // Adapter instance

    public Handler handler;     // for grabbing some event values for showing the dot

            // marker
    public ArrayList<String> items;     // container to store calendar items which needs showing the even marker

    public void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.calendar);

        month       = Calendar.getInstance();       // initialiZe month
        itemonth    = (Calendar) month.clone();     // initiaized to what month is

        items   = new ArrayList<String>();
        adapter = new CalendarAdapter(this, month);

        GridView gridview   = (GridView) findViewById(R.id.gridView);
        gridView.setAdapter(adapter);

        handler = new Handler();
        handler.post(calendarUpdaer);

        TextView title = (TextView) findViewById(R.id.title);
        title.setText(android.text.format.DateFormat.format("MMMM yyyy", month));

        RelativeLayout previous = (RelativeLayout) findViewById(R.id.previous);

        previous.setOnClickListener(new OnClickListener() {
         @Override
         public void onClick(View V) {
             setPreviousMonth();
             refreshCalendar();
            }
        });

        RelativeLayout next = (RelativeLayout) findViewById(R.id.next);

        next.setOnClickListener(new OnClickListener() {
         @Override
         public void onClick(View V) {
             setNextMonth();
             refreshCalendar();
            }
        });

        gridView.setOnItemClickListener(new OnItemClickListener() {
            public void onItemClick(AdapterView<?> parent, View V, int position, long id) {
                ((CalendarAdapter) parent.getAdapter()).setSelected(v);
                String selectedGridDate = CalendarAdapter.dayString.get(position);
                String[] separatedTime = separatedTime[2].replaceFirst("^0*", "");
            }
        });

        ((CalendarAdapter) parent.getAdapter()).setSelected(v);

        String      selectedGridDate    = CalendarAdapter.dayString.get(position);
        String []   separatedTime       = selectedGridDate.split("-");
        String      gridValueString     = separatedTime [2].replaceFirst("^0", "");     // taking last part of date. ie: 22 from 2015-10-23

        int gridValue   = Integer.parseInt(gridValueString);

        // navigate to next or previous month on clicking offdays
        if ((gridValue > 10) && (position < 8)) {
            setPreviousMonth();
            refreshCalendar();
        } else if ((gridValue < 7) && (position > 28)) {
            setNextMonth();
            refreshCalendar();
        }

        ((CalendarAdapter) parent.getAdapter()).setSelected(v);

        showToast(selectedGridDate);
    }

    protected void setNextMonth() {
        if (month.get(Calendar.MONTH) == month.getActualMaximum(Calendar.MONTH)) {
            month.set((month.get(Calendar.YEAR) + 1), month.getActualMinimum(Calendar.MONTH), 1);
        } else {
            month.set(Calendar.MONTH, month.get(Calendar.MONTH) + 1);
        }
    }

    protected void setPreviousMonth() {
        if (month.get(Calendar.MONTH) == month.getActualMinimum(Calendar.MONTH)) {
            month.set((month.get(Calendar.YEAR) - 1), month.getActualMaximum(Calendar.MONTH), 1);
        } else {
            month.set(Calendar.MONTH, month.get(Calendar.MONTH) - 1);
        }
    }

    protected void showToast(String str) {
        Toast.makeText(this, str, Toast.LENGTH_SHORT).show();
    }

    public void refreshCalendar() {
        TextView title  = (TextView) findViewById(R.id.title);

        adapter.refreshDays();
        adapter.notifyDateSetChanged();
        handler.post(calendarUpdater);  // generate some calendar items

        title.setText(android.text.format.DateFormat.format("MMMM yyyy", month));
    }

    public Runnable calendarUpdater = new Runnable() {
        @Override
        public void run() {
            items.clear();

            // Print dates of the current week
            DateFormat df   = new SimpleDateFormat("yyyy-MM-dd");
            String itemvalue;
            for (int i = 0; i < 7; i++) {
                itemvalue   = df.format(itemonth.getTime());
                itemonth.add(Calendar.DATE, 1);
                items.add("2015-10-26");
                items.add("2015-10-31");
                items.add("2015-11-08");
                items.add("2015-11-13");
                items.add("2015-12-24");
                items.add("2015-12-29");
            }

            adapter.setItems(items);
            adapter.notifyDataSetChanged();
        }
    };
}
