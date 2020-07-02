/**
 * 
 * @author 学校厕所类
 *
 */
public class washrool {
	private volatile boolean isAvaible=false;	//设置一个voatile方便可在线程中更改控制厕所的可用状态
	private  Object loke = new Object();		//厕所锁
	
	public boolean getisAvaible(){				//返回厕所是否可用
		return isAvaible;
	}
		
	public void setisAvaible(boolean available){ //更改其厕所是否可使用状态
		this.isAvaible=available;
	}
	
	public Object getloke(){						//返回锁
		return loke;
	}
}

