package p1;


import java.util.Objects;
import java.util.TreeSet;

public abstract class Student implements Comparable <Student> {

	String name;
	String Stream;

	public abstract int calculateMarks();

	public Student() {
		super();
	}

	public Student(String name, String stream) {
		super();
		this.name = name;
		Stream = stream;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public String getStream() {
		return Stream;
	}

	public void setStream(String stream) {
		Stream = stream;
	}

	@Override
	public int hashCode() {
		return Objects.hash(Stream, name);
	}

	@Override
	public boolean equals(Object obj) {
		if (this == obj)
			return true;
		if (obj == null)
			return false;
		if (getClass() != obj.getClass())
			return false;
		Student other = (Student) obj;
		return Objects.equals(Stream, other.Stream) && Objects.equals(name, other.name);
	}

	@Override
	public String toString() {
		return "Student [name=" + name + ", Stream=" + Stream + "]";
	}

}
