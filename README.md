# jubilant-succotash
Welcome to do any processing.


public class washrool {
	private volatile boolean isAvaible=false;	
	private  Object loke = new Object();		
	
	public boolean getisAvaible(){				
		return isAvaible;
	}
		
	public void setisAvaible(boolean available){
		this.isAvaible=available;
	}
	
	public Object getloke(){	
		return loke;
	}
}
