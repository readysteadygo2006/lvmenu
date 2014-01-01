package br.com.androidzin.android_examples;

import java.util.List;

import br.com.androidzin.android_examples.R;

import android.content.Context;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.ArrayAdapter;
import android.widget.ImageView;
import android.widget.TextView;

public class MySpinnerAdapter extends ArrayAdapter<SpinnerRow> {

	private List<SpinnerRow> rows;
	private int resource;

	public MySpinnerAdapter(Context context, int resource,
			int textViewResourceId, List<SpinnerRow> objects) {
		super(context, resource, textViewResourceId, objects);
		rows = objects;
		this.resource = resource;
	}

	static class ViewHolder {

		TextView text;
		ImageView icon;
	}

	@Override
	public View getDropDownView(int position, View convertView, ViewGroup parent) {
		ViewHolder  holder = new ViewHolder();
		if (convertView == null) {
			convertView = LayoutInflater.from(getContext()).inflate(resource,
					parent, false);
			
			holder.text = (TextView) convertView.findViewById(R.id.text);
			holder.icon = (ImageView) convertView.findViewById(R.id.icon);
			
			convertView.setTag(holder);

		} else {
			holder = (ViewHolder) convertView.getTag();
		}
		
		SpinnerRow currentRow = rows.get(position);
		holder.text.setText(currentRow.toString());
		holder.icon.setImageDrawable(
				getContext().getResources().getDrawable(currentRow.getIconResourceId()));
		
		
		return convertView;
	}

}
