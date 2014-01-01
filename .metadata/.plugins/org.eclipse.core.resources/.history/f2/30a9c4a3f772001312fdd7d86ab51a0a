package br.com.androidzin.android_examples;

import java.util.Random;

import android.os.Bundle;
import android.view.View;
import android.widget.TextView;

import com.actionbarsherlock.app.SherlockActivity;

public class RandomNumberActivity extends SherlockActivity{
	
	private static final Random RANDOM = new Random();
	private int count;
	
	private TextView numbers;
	
	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		
		setContentView(R.layout.random_numbers);
		count = 0;
		numbers = (TextView) findViewById(R.id.numbers);

	}

	
	public void generate(View button)
	{		
		int i = RANDOM.nextInt();
		count++;
		i = (i < 0 ? -i : i) % 7;
		
		String current = numbers.getText().toString();
		numbers.setText(current.concat(count+"º: " + i+",\n"));		
	}
}
