package br.com.androidzin.android_examples;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;

import com.actionbarsherlock.app.SherlockActivity;

public class MainActivity extends SherlockActivity {

	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.main);
	}
	
	public void startExample(View button)
	{
		Intent i = null;
		switch(button.getId())
		{
			case R.id.exampleSpinner:
				i = new Intent(getApplicationContext(), SpinnerIconActivity.class);
			break;
			
			case R.id.exampletRandom:
				i = new Intent(getApplicationContext(), SpinnerIconActivity.class);
			break;
			
			case R.id.exampletTimePicker:
				i = new Intent(getApplicationContext(), TimePickDifference.class);
			break;
			
			case R.id.exampleListWithIcon:
				i = new Intent(getApplicationContext(), ListWithIcon.class);
			break;
				
				
		}
		startActivity(i);
	}
	
	
	
	
}
