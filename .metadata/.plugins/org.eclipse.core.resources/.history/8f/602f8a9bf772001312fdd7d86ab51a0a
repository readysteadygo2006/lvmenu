package br.com.androidzin.android_examples;

import java.util.Calendar;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
import android.widget.TimePicker;
import android.widget.TimePicker.OnTimeChangedListener;

import com.actionbarsherlock.app.SherlockActivity;

public class TimePickDifference extends SherlockActivity implements OnTimeChangedListener{
	
	private TimePicker picker;
	private TextView sysCurrent;
	private TextView difference;
	
	private int pickedHour;
	private int pickedMinute;
	private Calendar calendar;
	
	private static final int hoursInMilis = 3600000;
	private static final int minutesInMilis = 60000;
	
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.timepicker);
		
		picker = (TimePicker) findViewById(R.id.picker);
		picker.setIs24HourView(true);
		picker.setOnTimeChangedListener(this);
		
		sysCurrent = (TextView) findViewById(R.id.systemTime);
		difference = (TextView) findViewById(R.id.difference);
		
	}
	
	@Override
	public void onTimeChanged(TimePicker view, int hourOfDay, int minute) {
		pickedHour = hourOfDay;
		pickedMinute = minute;
	}
	
	public void calculate(View view)
	{
		long currentTime = System.currentTimeMillis();
		long diffTime = 0;
		
		calendar = Calendar.getInstance();
		sysCurrent.setText(currentTime +"");
		
		calendar.setTimeInMillis(currentTime);
		calendar.set(Calendar.HOUR_OF_DAY, pickedHour);
		calendar.set(Calendar.MINUTE, pickedMinute);
		
		diffTime = calendar.getTimeInMillis()- currentTime;
		
		
		difference.setText(String.format("%02d:%02d",
				diffTime/hoursInMilis, 
				(diffTime%hoursInMilis)/minutesInMilis));
		
		
		
		
	}

}
