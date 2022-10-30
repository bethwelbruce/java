public class BinaryGap {
	public int solution(int N) {
		String bString=Integer.toString(N,2);
		//System.out.println(bString);
		boolean started = false;
		int counter = 0;
		int maxcount = 0;
		for(int i=0;i<bString.length();i++) {
			String c = bString.substring(i,i+1);
			if(c.equals("1")) {
				if(started) {
					if(counter>maxcount) {
						maxcount = counter;
					}
					
				}
				counter=0;
				started = true;
			}
			if(c.equals("0")) {
				counter++;
			}
			
		}
		
		return maxcount;
	}
	
	public static void main(String[] argd) {
		BinaryGap gb = new BinaryGap();
		System.out.println((gb.solution(9)));
	}
	

}
